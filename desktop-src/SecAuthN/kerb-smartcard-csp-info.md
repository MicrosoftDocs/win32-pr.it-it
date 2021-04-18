---
description: Contiene informazioni su un provider del servizio di crittografia (CSP) per smart card.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Struttura KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313295"
---
# <a name="kerb_smartcard_csp_info-structure"></a>\_Struttura delle \_ informazioni CSP per la smart card \_

La struttura di **\_ \_ \_ informazioni CSP** per la smart card di bordo contiene informazioni su un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per smart card.

Questa struttura non è dichiarata in un'intestazione pubblica.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**dwCspInfoLen**
</dt> <dd>

Dimensione, in byte, della struttura, inclusi i dati accodati.

</dd> <dt>

**MessageType**
</dt> <dd>

Tipo di messaggio passato. Questo membro deve essere impostato su 1.

</dd> <dt>

**ContextInformation**
</dt> <dd>

Riservato.

</dd> <dt>

**SpaceHolderForWow64**
</dt> <dd>

Riservato.

</dd> <dt>

**flags**
</dt> <dd>

Riservato.

</dd> <dt>

**KeySpec**
</dt> <dd>

Chiave privata da usare dal contenitore di chiavi specificato all'interno del buffer **bBuffer**. La chiave può essere uno dei valori seguenti, definiti in WinCrypt. h.



| Valore                                                                                                                                                                                                                   | Significato                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**Al \_ SCAMBIO**</dt> di stato <dt>1</dt> </dl> | La chiave è una chiave di scambio chiave.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**Al \_ FIRMA**</dt> <dt>2</dt> </dl>       | La chiave è una chiave di firma.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

Il numero di caratteri nel buffer **bBuffer** che precede il nome della smart card nel buffer.

> [!IMPORTANT]
> Se non viene specificato il nome della smart card, il buffer deve contenere una stringa vuota.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

Il numero di caratteri nel buffer **bBuffer** che precede il nome del lettore di smart card nel buffer.

> [!IMPORTANT]
> Se non viene specificato il nome del lettore di smart card, il buffer deve contenere una stringa vuota.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

Il numero di caratteri nel buffer **bBuffer** che precede il nome del contenitore di chiavi nel buffer. Questa stringa non può essere vuota.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

Il numero di caratteri nel buffer **bBuffer** che precede il nome del CSP nel buffer.

</dd> <dt>

**bBuffer**
</dt> <dd>

Matrice di caratteri inizializzata su una lunghezza di `sizeof(DWORD)` . Questo buffer contiene i nomi a cui fanno riferimento i membri **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** e **nCSPNameOffset** , nonché tutti i dati aggiuntivi forniti dal CSP.

Tutti i nomi non specificati devono essere rappresentati in questo buffer da stringhe vuote.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando questa struttura viene serializzata, i membri della struttura devono essere allineati ai limiti che sono multipli di 2 byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_accesso al certificato da marciapiede \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
