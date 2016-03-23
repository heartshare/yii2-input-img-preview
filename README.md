yii2-input-img-preview

Yii2 ElFinder input img preview

������ ��������� ����������� ElFinder Input. ��� ������������� ���������� ���� ��� ���������� �������� ���������� ������.

�������������:
use mihaildev\elfinder\InputFile;
use mihaildev\elfinder\ElFinder;
use xtarantulz\input-img-preview\InputImgPreview

echo $form->field($model, 'images')->widget(InputFile::className(), [
    'language'      => 'ru',
    'controller'    => 'elfinder', // ��������� �������� �����������, �� ��������� ����� elfinder
    'filter'        => 'image',    // ������ ������, ����� ������ ������ �������� https://github.com/Studio-42/elFinder/wiki/Client-configuration-options#wiki-onlyMimes
    'template'      => '<div class="input-group">{input}<span class="input-group-btn">{button}</span></div>',
    'options'       => ['class' => 'form-control'],
    'buttonOptions' => ['class' => 'btn btn-success'],
    'multiple'      => true       // ����������� ������ ���������� ������
]);
