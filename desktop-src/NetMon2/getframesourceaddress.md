---
description: Recupera l'indirizzo di origine di un frame.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Funzione GetFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305902"
---
# <a name="getframesourceaddress-function"></a>GetFrameSourceAddress (funzione)

La funzione **GetFrameSourceAddress** recupera l'indirizzo di origine di un frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* 
</dt> <dd>

Handle per il frame per il quale ottenere un puntatore.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Buffer restituito che archivia l'indirizzo di origine del frame.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo di indirizzo cercato, ad esempio indirizzo IP del tipo di indirizzo \_ \_ Ethernet o indirizzo \_ \_ IP.

</dd> <dt>

*Flag* 
</dt> <dd>

Flag utilizzati per modificare i dati dell'indirizzo di origine restituiti.



| Valore                                                                                                                                                                                                           | Significato                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**ADDRESSTYPE i \_ flag \_ normalizzati**</dt> </dl>        | Annulla il routing e i bit del gruppo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ flag di \_ bit \_ inverso**</dt> </dl> | Converte gli indirizzi di rete dell'anello di token al normale.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore *lpAddress* è valido e il valore restituito è BHERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                                | Descrizione                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**il \_ protocollo BHERR non è stato \_ \_ trovato**</dt> </dl> | Il protocollo specificato dal parametro *addressType* non è valido per il frame.<br/> |
| <dl> <dt>**\_HFRAME BHERR non valido \_**</dt> </dl>      | Il valore del parametro *hFrame* non è valido.<br/>                                        |



 

## <a name="remarks"></a>Commenti

È consentito un tipo di indirizzo di **\_ tipo indirizzo \_ \_ maggiore** . Quando viene usato questo tipo di indirizzo, la funzione Cerca l'indirizzo IP IPX, XNS, IP o VINES prima di restituire l'indirizzo ETHERNET, TOKENRING o FDDI. Questo approccio è utile per i protocolli e gli ambienti in cui è possibile multiplexare due schede di rete in un unico indirizzo del server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




