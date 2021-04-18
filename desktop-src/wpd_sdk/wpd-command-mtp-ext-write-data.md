---
description: Il comando WPD \_ comando \_ MTP \_ ext \_ Write \_ Data invia dati al dispositivo dopo l'esecuzione del comando WPD \_ Command \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ scrivere.
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: Comando WPD_COMMAND_MTP_EXT_WRITE_DATA (WpdMtpExtensions. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330565"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>Comando WPD \_ comando \_ MTP \_ ext \_ Write \_ Data

Il comando **WPD \_ comando \_ MTP \_ ext \_ Write \_ Data** invia dati al dispositivo dopo l'esecuzione del comando **WPD \_ Command \_ MTP \_ ext \_ Execute \_ \_ con \_ i dati \_ da \_ scrivere** .

## <a name="command-category"></a>Categoria

**WPD \_ categoria \_ MTP \_ \_ operazioni fornitore \_ ext**

## <a name="parameters"></a>Parametri

Per il driver sono previsti i parametri seguenti.



| Parametro                                                    | VarType             | Descrizione                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **Proprietà WPD del \_ \_ \_ contesto di trasferimento MTP ext \_ \_**               | \_LPWSTR VT          | Obbligatorio. Identifica il contesto restituito dalla chiamata precedente al dispositivo. |
| **\_Proprietà WPD \_ MTP \_ trasferimento EXT numero \_ \_ \_ \_ di byte da \_ scrivere** | \_UI4 VT             | Obbligatorio. Specifica il numero di byte da scrivere.                                      |
| **\_Proprietà WPD \_ MTP \_ \_ Transfer \_ Data**                  | VT \_ vettore \| VT \_ UI1 | Obbligatorio. Identifica il buffer in cui vengono copiati i dati del dispositivo.                  |



 

## <a name="return-value"></a>Valore restituito

Il driver restituisce i risultati seguenti.



| Risultato                                                     | VarType | Descrizione                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **\_Proprietà WPD \_ MTP \_ Transfer EXT numero \_ \_ \_ byte \_ scritti** | \_UI4 VT | Obbligatorio. Specifica il numero di byte inviati al dispositivo. |



 

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

 

 




