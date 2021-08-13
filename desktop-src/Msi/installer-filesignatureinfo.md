---
description: Il metodo FileSignatureInfo dell'oggetto Installer accetta il percorso di un file e restituisce un SAFEARRAY di byte che rappresentano l'hash o il certificato codificato.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Metodo Installer.FileSignatureInfo
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
ms.openlocfilehash: 670b5ba6deb4a53429180e832c2a49e4968c53efbe7c54cdf50e62e20bf5503b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630782"
---
# <a name="installerfilesignatureinfo-method"></a>Metodo Installer.FileSignatureInfo

Il **metodo FileSignatureInfo** dell'oggetto [**Installer**](installer-object.md) accetta il percorso di un file e restituisce un SAFEARRAY di byte che rappresentano l'hash o il certificato codificato. I valori possono quindi essere usati per popolare le tabelle [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md) [e MsiDigitalCertificate.](msidigitalcertificate-table.md)

Per altre informazioni, vedere il tipo [**di dati SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray).

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

*Filepath* 
</dt> <dd>

Percorso completo di un file con firma digitale.

Quando si popolano [le tabelle MsiDigitalSignature](msidigitalsignature-table.md) e [MsiDigitalCertificate,](msidigitalcertificate-table.md) *FilePath* punta a un file CAB con firma digitale. Quando si popolano [le tabelle MsiPatchCertificate](msipatchcertificate-table.md) e MsiDigitalCertificate, *FilePath* punta a una patch con firma digitale.

</dd> <dt>

*Opzioni* 
</dt> <dd>

Flag speciali per i casi di errore.



| Contrassegno                                                                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt> </dl> | Con *Options* impostato su msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** restituisce sempre un errore irreversibile per un hash non valido. <br/> Se *Options* non è impostato su msiSignatureOptionInvalidHashFatal e *Format* è impostato su msiSignatureInfoCertificate, **FileSignatureInfo** non restituisce un errore per un hash non valido.<br/> |



 

</dd> <dt>

*Formato* 
</dt> <dd>

Informazioni sulla firma richieste.



| Contrassegno                                                                                                                                                                                                                                                                                                        | Significato                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt> </dl> | Restituisce un SAFEARRAY di byte che rappresentano il certificato codificato.<br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <dt>**msiSignatureInfoHash**</dt> <dt>1</dt> </dl>                             | Restituisce un SAFEARRAY di byte che rappresentano l'hash.<br/>                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, il metodo restituisce [un SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) di byte che contengono l'hash o il certificato codificato.

## <a name="remarks"></a>Commenti

Per creare un'installazione firmata completamente verificata usando l'automazione, usare il metodo **FileSignatureInfo** per popolare le tabelle [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)e [MsiDigitalSignature.](msidigitalsignature-table.md) Per altre informazioni, vedere Creazione di un'installazione firmata [completamente verificata tramite Automazione.](authoring-a-fully-verified-signed-installation-using-automation.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Creazione di un'installazione firmata completamente verificata tramite Automazione](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[Digital Signatures and Windows Installer (Firme digitali e Windows programma di installazione)](digital-signatures-and-windows-installer.md)
</dt> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
