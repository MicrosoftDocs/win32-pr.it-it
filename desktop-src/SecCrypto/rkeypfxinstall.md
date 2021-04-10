---
description: La funzione RKeyPFXInstall non è supportata.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Funzione RKeyPFXInstall (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966697"
---
# <a name="rkeypfxinstall-function"></a>RKeyPFXInstall (funzione)

La funzione **RKeyPFXInstall** non è supportata.

**Windows Server 2003:** La funzione **RKeyPFXInstall** installa un certificato in un computer remoto. Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintassi


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hKeySvcCli* \[ in\]
</dt> <dd>

Handle [**di \_ handle KEYSVCC**](keysvcc-handle.md) precedentemente aperto da [**RKeyOpenKeyService**](rkeyopenkeyservice.md). L'handle rappresenta il computer remoto che riceverà il certificato. Questo valore non può essere **null**.

</dd> <dt>

*pPFX* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ BLOB KEYSVC**](keysvc-blob.md) che rappresenta il certificato da installare. Il BLOB è in formato [*PKCS \# 12*](../secgloss/p-gly.md) .

</dd> <dt>

*ppassword* \[ in\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ stringhe Unicode KEYSVC**](keysvc-unicode-string.md) che rappresenta la password per il BLOB. Al termine dell'utilizzo della password, cancellare la password dalla memoria chiamando la funzione [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Per ulteriori informazioni sulla protezione delle password, vedere [gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*ulFlags* \[ in\]
</dt> <dd>

Flag che specificano le opzioni di installazione del certificato. Questo parametro può essere uno zero o una combinazione dei valori seguenti.



| Valore                                                                                                                                                                                                                                     | Significato                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**Crypt \_ Esportabile**</dt><dt></dt> </dl>              | Le chiavi importate sono contrassegnate come esportabili.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**Crypt \_ \_keyset del computer**</dt><dt></dt> </dl> | Le chiavi private vengono archiviate nel computer remoto e non nell'utente corrente.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è \_ OK.

Se la funzione ha esito negativo, il valore restituito è un **ULONG** che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
