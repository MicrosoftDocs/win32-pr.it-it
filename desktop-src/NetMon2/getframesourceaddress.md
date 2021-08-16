---
description: Recupera l'indirizzo di origine di un frame.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Funzione GetFrameSourceAddress (Netmon.h)
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
ms.openlocfilehash: 4878e08b8d8fb475c0da23d2ed765819fa14a10cd93140c791ed8603b1677584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366318"
---
# <a name="getframesourceaddress-function"></a>Funzione GetFrameSourceAddress

La **funzione GetFrameSourceAddress** recupera l'indirizzo di origine di un frame.

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

Handle per il frame a cui ottenere un puntatore.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Buffer restituito che archivia l'indirizzo di origine del frame.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo di indirizzo cercato, ad esempio ADDRESS \_ TYPE \_ ETHERNET o ADDRESS \_ TYPE \_ IP.

</dd> <dt>

*Flag* 
</dt> <dd>

Flag utilizzati per modificare i dati dell'indirizzo di origine restituiti.



| Valore                                                                                                                                                                                                           | Significato                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**FLAG ADDRESSTYPE \_ \_ NORMALIZE**</dt> </dl>        | Annulla i BIT di routing e gruppo.<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**FLAG ADDRESSTYPE \_ \_ BIT \_ REVERSE**</dt> </dl> | Converte gli indirizzi di rete del token ring alla normalità.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il *valore lpAddress* è valido e il valore restituito è BHERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                                | Descrizione                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**PROTOCOLLO BHERR \_ \_ NON \_ TROVATO**</dt> </dl> | Il protocollo specificato dal *parametro AddressType* non è valido per il frame.<br/> |
| <dl> <dt>**HFRAME BHERR \_ NON \_ VALIDO**</dt> </dl>      | Il *valore del parametro hFrame* non è valido.<br/>                                        |



 

## <a name="remarks"></a>Commenti

È consentito un tipo **di indirizzo ADDRESS TYPE FIND \_ \_ \_ HIGHEST.** Quando si usa questo tipo di indirizzo, la funzione cerca l'indirizzo IPX, XNS, IP o VINES prima di restituire l'indirizzo ETHERNET, TOKENRING o FDDI. Questo approccio è utile per i protocolli e gli ambienti in cui è possibile eseguire il multiplexing di due schede di interfaccia di rete con un singolo indirizzo server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




