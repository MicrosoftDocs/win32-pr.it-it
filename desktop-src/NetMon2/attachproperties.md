---
description: La funzione di esportazione AttachProperties esegue il mapping delle proprietà a una posizione all'interno di una parte dei dati riconosciuti. AttachProperties deve essere implementato per ogni parser supportato dalla DLL del parser.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Funzione di callback AttachProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311642"
---
# <a name="attachproperties-callback-function"></a>Funzione di callback AttachProperties

La funzione di esportazione **AttachProperties** esegue il mapping delle proprietà a una posizione all'interno di una parte dei dati riconosciuti. **AttachProperties** deve essere implementato per ogni parser supportato dalla dll del parser.

## <a name="syntax"></a>Sintassi


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle del frame da analizzare.

</dd> <dt>

*lpFrame* \[ in\]
</dt> <dd>

Puntatore al primo byte in un frame.

</dd> <dt>

*lpProtocol* \[ in\]
</dt> <dd>

Puntatore all'inizio dei dati riconosciuti.

</dd> <dt>

*MacType* \[ in\]
</dt> <dd>

Valore MAC del primo protocollo in un frame. *MacType* può essere uno dei seguenti:



| Valore                                                                                                                                                                         | Significato                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**\_Ethernet di tipo Mac \_**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**\_Tokenring di tipo Mac \_**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**\_FDDI di tipo Mac \_**</dt> </dl>                | ANSI X3T 9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ in\]
</dt> <dd>

Numero rimanente di byte in un frame a partire dall'inizio dei dati riconosciuti.

</dd> <dt>

*hPreviousProtocol* \[ in\]
</dt> <dd>

Handle del protocollo precedente.

</dd> <dt>

*nPreviousProtocolOffset* \[ in\]
</dt> <dd>

Offset del protocollo precedente a partire dall'inizio del frame.

</dd> <dt>

*lpInstData* \[ in\]
</dt> <dd>

Puntatore ai dati dell'istanza forniti dal protocollo precedente. I dati dell'istanza non possono essere più lunghi di un \_ ptr DWORD di lunghezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte dopo i dati riconosciuti in un frame o **null** se i dati riconosciuti sono l'ultima parte di dati di un frame.

Se la funzione ha esito negativo, il valore restituito è un puntatore ai dati riconosciuti. Il parametro *lpProtocol* passa il puntatore alla DLL del parser.

## <a name="remarks"></a>Commenti

Network Monitor chiama la funzione **AttachProperties** per ogni parser che riconosce una porzione di dati in un frame. Si noti che il parser determina quali proprietà sono presenti nei dati riconosciuti e dove si trova ogni proprietà.

Durante l'implementazione di **AttachProperties**, chiamare [AttachPropertyInstance](attachpropertyinstance.md) per usare i dati esistenti nell'acquisizione. È anche possibile chiamare la funzione [AttachPropertyInstanceEx](attachpropertyinstanceex.md) per modificare i dati della proprietà. Tuttavia, si consiglia di usare i dati esistenti nell'acquisizione.

Le funzioni **AttachPropertyInstanceEx** e **AttachPropertyInstance** vengono chiamate solo per le proprietà presenti nei dati riconosciuti. Si noti che Network Monitor dispone di un [*database delle proprietà*](p.md) per il parser che contiene una descrizione di tutte le proprietà supportate dal parser.

**Dati dell'istanza**

I dati dell'istanza sono informazioni passate da un parser a un altro. I dati dell'istanza possono essere dati di lunghezza minore o uguale a un \_ ptr DWORD o un puntatore ai dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal parser. Nel parametro *lpInstData* delle funzioni **AttachProperties** e [RecognizeFrame](recognizeframe.md) Network Monitor fornisce un puntatore ai dati dell'istanza del protocollo precedente. È possibile impostare i dati dell'istanza per il parser durante l'implementazione di **RecognizeFrame**.



| Per informazioni su                                          | Vedere                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor.   | [Parser](parsers.md)                                             |
| Punti di ingresso inclusi nella DLL del parser.           | [Architettura DLL parser](parser-dll-architecture.md)             |
| Come riconoscere i dati.                                      | [Implementazione di RecognizeFrame](implementing-recognizeframe.md)     |
| Come creare un database di proprietà.                          | [Implementazione del registro](implementing-register.md)                 |
| L'implementazione di **AttachProperties**  include un esempio. | [Implementazione di AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




