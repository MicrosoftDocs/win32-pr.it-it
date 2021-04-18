---
description: Il metodo FileSignatureInfo dell'oggetto Installer accetta il percorso di un file e restituisce un SAFEARRAY di byte che rappresenta l'hash o il certificato codificato.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer. FileSignatureInfo, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324625"
---
# <a name="installerfilesignatureinfo-method"></a>Installer. FileSignatureInfo, metodo

Il metodo **FileSignatureInfo** dell'oggetto [**Installer**](installer-object.md) accetta il percorso di un file e restituisce un SAFEARRAY di byte che rappresenta l'hash o il certificato codificato. I valori possono quindi essere usati per popolare le tabelle [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalCertificate](msidigitalcertificate-table.md) .

Per ulteriori informazioni, vedere il [**tipo di dati SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).

## <a name="syntax"></a>Sintassi


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FilePath* 
</dt> <dd>

Percorso completo di un file con firma digitale.

Quando si popolano le tabelle [MsiDigitalSignature](msidigitalsignature-table.md) e [MsiDigitalCertificate](msidigitalcertificate-table.md) , *filePath* punta a un cabinet con firma digitale. Quando si popolano le tabelle [MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate, *filePath* punta a una patch con firma digitale.

</dd> <dt>

*Opzioni* 
</dt> <dd>

Flag speciali per i casi di errore.



| Contrassegno                                                                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Con le *Opzioni* impostate su MsiSignatureOptionInvalidHashFatal, **FileSignatureInfo** restituisce sempre un errore irreversibile per un hash non valido. <br/> Se *options* non è impostato su MsiSignatureOptionInvalidHashFatal e *Format* è impostato su msiSignatureInfoCertificate, **FileSignatureInfo** non restituisce un errore per un hash non valido.<br/> |



 

</dd> <dt>

*Formato* 
</dt> <dd>

Informazioni sulla firma richieste.



| Contrassegno                                                                                                                                                                                                                                                                                                        | Significato                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Restituisce un SAFEARRAY di byte che rappresenta il certificato codificato.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Restituisce un SAFEARRAY di byte che rappresenta l'hash.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, il metodo restituisce un [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) di byte che contiene il certificato hash o codificato.

## <a name="remarks"></a>Commenti

Per creare un'installazione firmata completamente verificata tramite l'automazione, utilizzare il metodo **FileSignatureInfo** per popolare le tabelle [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalSignature](msidigitalsignature-table.md) . Per altre informazioni, vedere [creazione di un'installazione firmata completamente verificata usando l'automazione](authoring-a-fully-verified-signed-installation-using-automation.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Creazione di un'installazione firmata completamente verificata tramite l'automazione](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Firme digitali e Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
