---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Read \_ Data recupera i dati dal dispositivo dopo l'esecuzione del comando WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ leggere.
ms.assetid: d7acb2cc-28b0-4314-99fd-4e7eded22122
title: Comando WPD_COMMAND_MTP_EXT_READ_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671101ee9be6e355a4e64d2a467d83d0028db69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330567"
---
# <a name="wpd_command_mtp_ext_read_data-command"></a>Comando WPD \_ comando \_ MTP \_ ext \_ Read \_ Data

Il comando **WPD \_ comando \_ MTP \_ ext \_ Read \_ Data** recupera i dati dal dispositivo dopo l'esecuzione del comando **WPD \_ comando \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ leggere** .

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                                   | VarType             | Descrizione                                                                            |
|-------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**              | \_LPWSTR VT          | Obbligatorio. Identifica il contesto restituito dalla chiamata precedente al dispositivo. |
| **\_Proprietà WPD \_ MTP \_ trasferimento ext ext numero \_ \_ \_ \_ di byte da \_ leggere** | \_UI4 VT             | Obbligatorio. Specifica il numero di byte da leggere.                                       |
| **\_Proprietà WPD \_ MTP \_ \_ Transfer \_ Data**                 | VT \_ vettore \| VT \_ UI1 | Obbligatorio. Identifica il buffer in cui vengono copiati i dati del dispositivo.                  |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                  | VarType             | Descrizione                                                       |
|---------------------------------------------------------|---------------------|-------------------------------------------------------------------|
| **\_Proprietà WPD \_ MTP Transfer numero di \_ \_ \_ \_ byte \_ letti** | \_UI4 VT             | Obbligatorio. Specifica il numero di byte ricevuti dal dispositivo. |
| **\_Proprietà WPD \_ MTP \_ \_ Transfer \_ Data**             | VT \_ vettore \| VT \_ UI1 | Obbligatorio. Buffer che contiene i dati del dispositivo.               |



 

## <a name="calling-methods"></a>Chiamata di metodi

Può essere chiamato solo direttamente tramite [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>WpdMtpExtensions. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




