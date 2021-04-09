---
title: Altre costanti di sessione (WSManDisp. h)
description: Specificare la codifica, la crittografia e la porta nome entità servizio.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 236e69d80db2ad30b8cc2934b6b2016d7eecbed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121071"
---
# <a name="other-session-constants"></a>Altre costanti di sessione

Costanti, elencate nell'elenco seguente, nell'enumerazione **\_ \_ WSManSessionFlags** che specificano la porta di codifica, crittografia e nome dell'entità servizio.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Invia la richiesta in UTF8 anziché UTF16.

Il metodo di scripting associato è [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) e il metodo C++ è [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Non crittografare i messaggi inviati in rete. Questa impostazione è consentita solo se il [*listener*](windows-remote-management-glossary.md) è configurato in modo che **AllowUnencrypted** sia impostato su **true**.

Il metodo di scripting associato è [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) e il metodo C++ è [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Specificare la porta del nome dell'entità servizio (SPN) per la connessione diretta a hardware BMC remoto, nota anche come connessione [*fuori banda*](windows-remote-management-glossary.md) . Poiché sia il computer server WinRM che l'hardware BMC possono condividere lo stesso indirizzo IP, questo flag indica che il numero di porta SPN deve essere utilizzato per determinare se la connessione è al servizio o direttamente al BMC. Per ulteriori informazioni, vedere [formati dei nomi per nomi SPN univoci](/windows/desktop/AD/name-formats-for-unique-spns).

Il metodo di scripting associato è [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) e il metodo C++ è [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



Invia la richiesta in UTF16.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sessione](session-constants.md)
</dt> </dl>

 

