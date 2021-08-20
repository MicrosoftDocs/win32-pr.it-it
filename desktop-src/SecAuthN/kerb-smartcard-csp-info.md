---
description: Contiene informazioni su un smart card provider del servizio di crittografia (CSP).
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO struttura
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
ms.openlocfilehash: 190c3e770a50acb7363fb10c469a7400831bc7b512d2b8158d687c83403b6df9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127341"
---
# <a name="kerb_smartcard_csp_info-structure"></a>Struttura KERB \_ SMARTCARD \_ CSP \_ INFO

La **struttura KERB \_ SMARTCARD \_ CSP \_ INFO** contiene informazioni su smart card [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).

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

Dimensione, in byte, di questa struttura, inclusi i dati accodati.

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

Chiave privata da usare dal contenitore di chiavi specificato all'interno del buffer **bBuffer**. La chiave può essere uno dei valori seguenti, definiti in WinCrypt.h.



| Valore                                                                                                                                                                                                                   | Significato                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> <dt>1</dt> </dl> | La chiave è una chiave di scambio delle chiavi.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ FIRMA**</dt> <dt>2</dt> </dl>       | La chiave è una chiave di firma.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

Numero di caratteri nel buffer **bBuffer** che precedono il nome del smart card nel buffer.

> [!IMPORTANT]
> Se il nome del smart card non viene specificato, il buffer deve contenere una stringa vuota.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

Numero di caratteri nel buffer **bBuffer** che precedono il nome del smart card lettore nel buffer.

> [!IMPORTANT]
> Se il nome del smart card lettore non viene specificato, il buffer deve contenere una stringa vuota.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

Numero di caratteri nel buffer **bBuffer** che precedono il nome del contenitore di chiavi in tale buffer. Questa stringa non può essere vuota.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

Numero di caratteri nel buffer **bBuffer** che precedono il nome del provider di servizi di configurazione nel buffer.

</dd> <dt>

**bBuffer**
</dt> <dd>

Matrice di caratteri inizializzata su una lunghezza di `sizeof(DWORD)` . Questo buffer contiene i nomi a cui fa riferimento i membri **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** e **nCSPNameOffset,** nonché eventuali dati aggiuntivi forniti dal provider di servizi di configurazione.

Tutti i nomi non specificati devono essere rappresentati in questo buffer da stringhe vuote.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando questa struttura viene serializzata, i membri della struttura devono essere allineati a limiti multipli di 2 byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ACCESSO AL CERTIFICATO KERB \_ \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
