---
description: Recupera il profilo di convalida della piattaforma per una protezione con chiave specificata del tipo appropriato.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Metodo GetKeyProtectorPlatformValidationProfile della classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316104"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Metodo GetKeyProtectorPlatformValidationProfile della \_ classe EncryptableVolume Win32

Il metodo **GetKeyProtectorPlatformValidationProfile** Recupera il profilo di convalida della piattaforma per una protezione con chiave specificata del tipo appropriato.

L'identificatore della protezione con chiave deve fare riferimento a una protezione con chiave di tipo "TPM", "TPM e PIN", "TPM, PIN e chiave di avvio" oppure "TPM e chiave di avvio".

## <a name="syntax"></a>Sintassi


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VolumeKeyProtectorID* \[ in\]
</dt> <dd>

Tipo: **stringa**

Identificatore di stringa univoco utilizzato per gestire una protezione con chiave del volume crittografata.

</dd> <dt>

*PlatformValidationProfile* \[ out\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice di valori integer che specifica il modo in cui l'hardware di sicurezza del Trusted Platform Module (TPM) del computer protegge la chiave di crittografia del volume del disco.



| Valore                                                                         | Significato                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Radice principale di Trust of Measurement (CRTM), BIOS ed estensioni della piattaforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configurazione e dati della piattaforma e della scheda madre<br/>                         |
| <dl> <dt>2</dt> </dl>  | Codice ROM opzione<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configurazione e dati dell'opzione ROM<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Codice MBR (master boot record)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabella di partizione MBR (record di avvio principale)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Eventi di riattivazione e transizione di stato<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Manufacturer-Specific computer<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Settore di avvio NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Blocco di avvio NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Gestione avvio<br/>                                                            |
| <dl> <dt>11</dt> </dl> | Controllo di accesso di BitLocker<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                          |
| <dl> <dt>13</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                          |
| <dl> <dt>14</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                          |
| <dl> <dt>15</dt> </dl> | Definito per l'utilizzo da parte del sistema operativo statico<br/>                          |
| <dl> <dt>16</dt> </dl> | Usato per il debug<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinamico<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Piattaforma definita<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>21</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usato da un sistema operativo attendibile<br/>                                      |
| <dl> <dt>23</dt> </dl> | Supporto delle applicazioni<br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei codici seguenti o un altro codice di errore se ha esito negativo.



| Codice/valore restituito                                                                                                                                                                  | Descrizione                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | Il metodo è stato eseguito correttamente.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | Il parametro *VolumeKeyProtectorID* non fa riferimento a una protezione con chiave di tipo "TPM", "TPM e pin", "TPM, pin e chiave di avvio" oppure "TPM e chiave di avvio".<br/> |
| <dl> <dt>**FVE \_ E \_ non \_ attivato**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | Nel volume non è abilitato BitLocker. Aggiungere una protezione con chiave per abilitare BitLocker.<br/>                                                                                  |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/>                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
