---
description: Nella tabella seguente sono elencati tutti i valori HRESULT che possono essere restituiti dai metodi nell'API di firma digitale XPS.
ms.assetid: d20707b0-55ea-438a-8ce3-972c61678928
title: Errori dell'API di firma digitale XPS (Xpsdigitalsignature.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e40cea4b7d0e9997157c8b18c7f364ac7ac58b2b9edc6faec62cbe98685fcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711361"
---
# <a name="xps-digital-signature-api-errors"></a>Errori dell'API di firma digitale XPS

Nella tabella seguente sono **elencati tutti i valori HRESULT** che possono essere restituiti dai metodi nell'API di firma digitale XPS. Si noti che non tutti i metodi possono restituire tutti i valori restituiti elencati in questa tabella.



| Codice/valore restituito                                                                                                                                                                                                                                                                                  | Descrizione                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                                                                                                                 | Il metodo è riuscito.<br/>                                                                                                                                                  |
| <span id="XPS_E_INVALID_SIGNATUREBLOCK_MARKUP"></span><span id="xps_e_invalid_signatureblock_markup"></span><dl> <dt>**XPS \_ E \_ MARKUP \_ SIGNATUREBLOCK \_ NON**</dt> <dt>VALIDO 0x8052038b</dt> </dl> | Si è verificato un errore nel markup XML del blocco di firma durante la lettura del markup della firma.<br/>                                                               |
| <span id="XPS_E_MARKUP_COMPATIBILITY_ELEMENTS"></span><span id="xps_e_markup_compatibility_elements"></span><dl> <dt>**XPS \_ ELEMENTI DI \_ \_ COMPATIBILITÀ \_ DEL MARKUP E**</dt> <dt>0X80520389</dt> </dl> | Il [**valore XPS \_ SIGN \_ FLAGS**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_flags) ha specificato che non era previsto alcun elemento di compatibilità del markup. Tuttavia, sono stati trovati elementi di compatibilità del markup.<br/> |
| <span id="XPS_E_OBJECT_DETACHED"></span><span id="xps_e_object_detached"></span><dl> <dt>**XPS \_ E \_ OBJECT \_ DETACHED**</dt> <dt>0x8052038a</dt> </dl>                                            | L'interfaccia non è associata al gestore delle firme.<br/>                                                                                                            |
| <span id="XPS_E_PACKAGE_ALREADY_OPENED"></span><span id="xps_e_package_already_opened"></span><dl> <dt>**XPS \_ E \_ PACCHETTO GIÀ APERTO \_ \_ 0X80520387**</dt> <dt></dt> </dl>                      | Un pacchetto XPS è già stato aperto nel gestore delle firme. <br/>                                                                                                      |
| <span id="XPS_E_PACKAGE_NOT_OPENED"></span><span id="xps_e_package_not_opened"></span><dl> <dt>**XPS \_ E \_ PACCHETTO \_ NON \_ APERTO**</dt> <dt>0X80520386</dt> </dl>                                  | Un pacchetto XPS non è ancora stato aperto nel gestore delle firme. <br/>                                                                                                      |
| <span id="XPS_E_SIGNATUREID_DUP"></span><span id="xps_e_signatureid_dup"></span><dl> <dt>**XPS \_ E \_ SIGNATUREID \_ DUP**</dt> <dt>0x80520388</dt> </dl>                                            | Due o più firme hanno lo stesso ID.<br/>                                                                                                                               |
| <span id="XPS_E_SIGREQUESTID_DUP"></span><span id="xps_e_sigrequestid_dup"></span><dl> <dt>**XPS \_ E \_ SIGREQUESTID \_ DUP**</dt> <dt>0x80520385</dt> </dl>                                         | L'ID richiesta di firma non è univoco all'interno del blocco della firma.<br/>                                                                                                     |



 

## <a name="remarks"></a>Commenti

Alcuni metodi dell'API di firma digitale XPS effettuano chiamate all'API [di creazione pacchetti.](/previous-versions/windows/desktop/opc/packaging) Per informazioni sui valori restituiti dell'API di creazione pacchetti, vedere [Errori di creazione pacchetti.](/previous-versions/windows/desktop/opc/packaging-errors)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                            |
| Intestazione<br/>                   | <dl> <dt>Xpsdigitalsignature.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>XpsDigitalSignature.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione degli errori in COM](../com/error-handling-in-com.md)
</dt> <dt>

[Errori di creazione pacchetti](/previous-versions/windows/desktop/opc/packaging-errors)
</dt> <dt>

[Valori restituiti dalla crittografia](/windows/desktop/SecCrypto/cryptography-return-values)
</dt> </dl>

 

