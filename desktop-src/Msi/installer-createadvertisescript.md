---
description: Il metodo CreateAdvertiseScript dell'oggetto Installer genera uno script di annuncio.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Metodo Installer:: CreateAdvertiseScript'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333880"
---
# <a name="installercreateadvertisescript-method"></a>Metodo Installer:: CreateAdvertiseScript

Il metodo **CreateAdvertiseScript** dell'oggetto [**Installer**](installer-object.md) genera uno script di annuncio.

## <a name="syntax"></a>Sintassi


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packagePath* 
</dt> <dd>

Percorso completo del pacchetto di Windows Installer (MSI) da annunciare.

</dd> <dt>

*scriptFilePath* 
</dt> <dd>

Percorso completo del file di script da creare con le informazioni annunciate.

</dd> <dt>

*trasforma* 
</dt> <dd>

Elenco di trasformazioni da applicare al prodotto. Le trasformazioni nell'elenco sono delimitate da punti e virgola. Questo parametro è facoltativo.

</dd> <dt>

*language* 
</dt> <dd>

Lingua del pacchetto di installazione da usare. Questo parametro è facoltativo.

</dd> <dt>

*platform* 
</dt> <dd>

Questo parametro specifica per quale piattaforma il programma di installazione deve creare lo script. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                                                       | Significato                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt> </dl> | Crea uno script per la piattaforma corrente.<br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt> </dl>                 | Crea uno script per la piattaforma x86.<br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt> </dl>             | Crea uno script per sistemi basati su Itanium.<br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt> </dl>                 | Crea uno script per la piattaforma x64.<br/>      |



 

</dd> <dt>

*options* 
</dt> <dd>

Opzioni dell'annuncio. Questo parametro è facoltativo. Questo parametro può avere uno dei valori seguenti. Questo parametro è facoltativo.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Annuncio standard<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Annuncia una nuova istanza del prodotto. Richiede che la prima trasformazione nell'elenco di trasformazione del parametro *transforms* sia la trasformazione dell'istanza che modifica il codice del prodotto. Per ulteriori informazioni, vedere [installazione di più istanze di prodotti e patch](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il metodo [**AdvertiseProduct**](installer-advertiseproduct.md) usa la funzione [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo del metodo **CreateAdvertiseScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




