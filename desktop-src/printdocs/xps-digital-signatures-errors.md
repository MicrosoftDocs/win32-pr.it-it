---
description: Nella tabella seguente sono elencati tutti i valori HRESULT che possono essere restituiti dai metodi nell'API per la firma digitale XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Errori dell'API firma digitale XPS (XpsDigitalSignature. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c82c6f5efe7e67d27f7d94b5d1db2732139fa59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348211"
---
# <a name="xps-digital-signature-api-errors"></a>Errori dell'API firma digitale XPS

Nella tabella seguente sono elencati tutti i valori **HRESULT** che possono essere restituiti dai metodi nell'API per la firma digitale XPS. Si noti che non tutti i metodi possono restituire tutti i valori restituiti elencati in questa tabella.



| Codice/valore restituito                                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**\_OK**</dt> </dl>                                                                                                                                                                 | Il metodo è riuscito.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ \_ SIGNATUREBLOCK \_ markup 0x8052038b non valido**</dt> <dt></dt> </dl> | Si è verificato un errore nel markup XML del blocco della firma durante la lettura del markup della firma.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ \_Elementi di \_ compatibilità \_ del markup E**</dt> <dt>0x80520389</dt> </dl> | Il valore dei [**\_ \_ flag di firma XPS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) ha specificato che non sono previsti elementi di compatibilità del markup. sono stati tuttavia trovati elementi di compatibilità del markup.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E \_ oggetto \_ scollegato**</dt> <dt>0x8052038a</dt> </dl>                                            | L'interfaccia non è associata alla gestione della firma.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ Pacchetto di E \_ \_ già \_ aperto**</dt> <dt>0x80520387</dt> </dl>                      | Un pacchetto XPS è già stato aperto in gestione firme. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ \_Pacchetto E \_ non \_ aperto**</dt> <dt>0x80520386</dt> </dl>                                  | Un pacchetto XPS non è ancora stato aperto in gestione firme. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Due o più firme hanno lo stesso ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | L'ID richiesta di firma non è univoco all'interno del blocco della firma.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Alcuni metodi API per la firma digitale XPS effettuano chiamate all'API di creazione dei [pacchetti](/previous-versions/windows/desktop/opc/packaging) . Per informazioni sui valori restituiti dell'API di creazione pacchetti, vedere errori di creazione [pacchetti](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                            |
| Intestazione<br/>                   | <dl> <dt>XpsDigitalSignature. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>XpsDigitalSignature. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione degli errori in COM](../com/error-handling-in-com.md)
</dt> <dt>

[Errori di creazione pacchetto](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valori restituiti della crittografia](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

