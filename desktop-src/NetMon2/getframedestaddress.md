---
description: Recupera l'indirizzo di destinazione di un frame.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Funzione GetFrameDestAddress (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: d7719392794027567521ce3e9c1bd1caf8ecbf76110f76ad0e54e0dd6549aae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366626"
---
# <a name="getframedestaddress-function"></a>Funzione GetFrameDestAddress

La **funzione GetFrameDestAddress** recupera l'indirizzo di destinazione di un frame.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI GetFrameDestAddress(
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

Handle del frame a cui ottenere un puntatore.

</dd> <dt>

*lpAddress* 
</dt> <dd>

Buffer restituito che archivia l'indirizzo di destinazione del frame.

</dd> <dt>

*AddressType* 
</dt> <dd>

Tipo di indirizzo, ad esempio ADDRESS \_ TYPE \_ ETHERNET o ADDRESS \_ TYPE \_ IP.

</dd> <dt>

*Flag* 
</dt> <dd>

Flag utilizzati per modificare i dati dell'indirizzo di destinazione restituiti.



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
| <dl> <dt>**PROTOCOLLO BHERR \_ \_ NON \_ TROVATO**</dt> </dl> | Il protocollo specificato nel *parametro AddressType* non è valido per il frame.<br/> |
| <dl> <dt>**HFRAME BHERR \_ NON \_ VALIDO**</dt> </dl>      | Il *valore hFrame* non è valido.<br/>                                                  |



 

## <a name="remarks"></a>Commenti

Il **tipo di indirizzo ADDRESS TYPE FIND \_ \_ \_ HIGHEST** è consentito. Quando si usa questo tipo di indirizzo, la funzione cerca l'indirizzo IPX, XNS, IP o VINES prima di restituire l'indirizzo ETHERNET, TOKENRING o FDDI. Questo approccio è utile per i protocolli e negli ambienti in cui è possibile eseguire il multiplexing di due schede di interfaccia di rete con un singolo indirizzo server.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




