---
description: Definisce un singolo oggetto di un filtro di visualizzazione.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Struttura FILTEROBJECT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305934"
---
# <a name="filterobject-structure"></a>Struttura FILTEROBJECT

La struttura **FILTEROBJECT** definisce un singolo oggetto di un filtro di visualizzazione. La funzione [**FilterAddObject**](filteraddobject.md) USA **FILTEROBJECT** per creare un filtro di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a>Members

<dl> <dt>

**Azione**
</dt> <dd>

Flag che specifica l'azione **FILTEROBJECT** . Un flag può specificare una proprietà, un valore o un operatore.

Nella tabella seguente sono elencati i flag delle proprietà dei membri di azione.



| Valore                                                                                                                                                                                                | Significato                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <dt>**\_Proprietà FILTERACTION**</dt> </dl>                | Contiene questa proprietà.<br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <dt>**\_PROPERTYEXIST FILTERACTION**</dt> </dl> | Indica che una proprietà di azione filtro è già definita.<br/> |



 

Nella tabella seguente sono elencati i flag dei valori dei membri di azione.



| Valore                                                                                                                                                                                        | Significato                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <dt>**\_valore FILTERACTION**</dt> </dl>                 | Contiene questo valore.<br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <dt>**\_stringa FILTERACTION**</dt> </dl>              | Contiene questa stringa.<br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <dt>**\_matrice FILTERACTION**</dt> </dl>                 | Contiene questa matrice.<br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <dt>**\_CONTAINSNC FILTERACTION**</dt> </dl>  | Indica che una proprietà contiene una sottostringa senza distinzione tra maiuscole e minuscole.<br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <dt>**FILTERACTION \_ contiene**</dt> </dl>        | Indica che una proprietà contiene una sottostringa con distinzione tra maiuscole e minuscole.<br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <dt>**\_Indirizzo FILTERACTION**</dt> </dl>           | Contiene l'indirizzo MAC.<br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <dt>**\_ADDRESSANY FILTERACTION**</dt> </dl>  | Corrisponde a qualsiasi indirizzo MAC.<br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <dt>**FILTERACTION \_ da**</dt> </dl>                    | Indica l'indirizzo **Mac da** .<br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <dt>**FILTERACTION \_**</dt> </dl>                          | Indica l'indirizzo **Mac** .<br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <dt>**\_FROMTO FILTERACTION**</dt> </dl>              | Indica un'associazione **tra/** e di indirizzi Mac.<br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <dt>**\_largeInt FILTERACTION**</dt> </dl>        | Contiene un numero intero grande.<br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <dt>**FILTERACTION \_ tempo**</dt> </dl>                    | Contiene una struttura **SYSTEMTIME** .<br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <dt>**FILTERACTION \_ addr \_**</dt> </dl> | Contiene un indirizzo MAC Ethernet.<br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <dt>**\_token addr \_ FILTERACTION**</dt> </dl> | Contiene un indirizzo MAC dell'anello di token.<br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <dt>**FILTERACTION \_ addr \_ FDDI**</dt> </dl>    | Contiene un indirizzo MAC di FDDI.<br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <dt>**FILTERACTION \_ addr \_ IPX**</dt> </dl>       | Contiene un indirizzo MAC IPX.<br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <dt>**\_IP addr \_ FILTERACTION**</dt> </dl>          | Contiene un indirizzo MAC IP.<br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <dt>**\_OID FILTERACTION**</dt> </dl>                       | Contiene un identificatore di oggetto (OID).<br/>                             |



 

Nella tabella seguente sono elencati i flag dell'operatore membro di azione.



| Valore                                                                                                                                                                                                        | Significato                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <dt>**FILTERACTION \_ non valido**</dt> </dl>                           | Indica un'azione di filtro non valida.<br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <dt>**FILTERACTION \_ e**</dt> </dl>                                       | Indica un'istruzione **and** logica.<br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <dt>**FILTERACTION \_ o**</dt> </dl>                                          | Indica un'istruzione **or** logica.<br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <dt>**\_Xor FILTERACTION**</dt> </dl>                                       | Indica un'istruzione **or** esclusivo logica (XOR).<br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <dt>**FILTERACTION \_**</dt> </dl>                                       | Indica un'istruzione **not** logica.<br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <dt>**\_EQUALNC FILTERACTION**</dt> </dl>                           | L'azione filtro è uguale e senza distinzione tra maiuscole e minuscole.<br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <dt>**FILTERACTION \_ uguale a**</dt> </dl>                                 | L'azione filtro è uguale e maiuscole/minuscole.<br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <dt>**\_NOTEQUALNC FILTERACTION**</dt> </dl>                  | L'istruzione NOT logica è uguale e **senza** distinzione tra maiuscole e minuscole.<br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <dt>**\_NOTEQUAL FILTERACTION**</dt> </dl>                        | L'istruzione **not** logica è uguale e fa distinzione tra maiuscole e minuscole.<br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <dt>**\_GREATERNC FILTERACTION**</dt> </dl>                     | L'azione di filtro è maggiore di (>) e senza distinzione tra maiuscole e minuscole.<br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <dt>**FILTERACTION \_ maggiore**</dt> </dl>                           | L'azione di filtro è maggiore di (>) e distinzione tra maiuscole e minuscole.<br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <dt>**\_LESSNC FILTERACTION**</dt> </dl>                              | L'azione di filtro è minore di (<) e senza distinzione tra maiuscole e minuscole.<br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <dt>**FILTERACTION \_ less**</dt> </dl>                                    | L'azione di filtro è minore di (<) e distinzione tra maiuscole e minuscole.<br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <dt>**\_GREATEREQUALNC FILTERACTION**</dt> </dl>      | L'azione di filtro è maggiore o uguale a (>=) e senza distinzione tra maiuscole e minuscole.<br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <dt>**\_GREATEREQUAL FILTERACTION**</dt> </dl>            | L'azione di filtro è maggiore o uguale a (>=) e con distinzione tra maiuscole e minuscole.<br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <dt>**\_LESSEQUALNC FILTERACTION**</dt> </dl>               | L'azione di filtro è minore o uguale a (<=) e senza distinzione tra maiuscole e minuscole.<br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <dt>**\_LESSEQUAL FILTERACTION**</dt> </dl>                     | L'azione di filtro è minore o uguale a (<=) e fa distinzione tra maiuscole e minuscole.<br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <dt>**FILTERACTION \_ Plus**</dt> </dl>                                    | Operatore Add (+).<br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <dt>**FILTERACTION \_ meno**</dt> </dl>                                 | Operatore di sottrazione (-).<br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <dt>**\_AREBITSON FILTERACTION**</dt> </dl>                     | Indica un'operazione bit per bit.<br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <dt>**\_AREBITSOFF FILTERACTION**</dt> </dl>                  | Indica un'operazione non bit per bit.<br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <dt>**\_PROTOCOLSEXIST FILTERACTION**</dt> </dl>      | Indica che i protocolli selezionati sono disponibili.<br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <dt>**\_PROTOCOLEXIST FILTERACTION**</dt> </dl>         | Indica che il protocollo selezionato esiste.<br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <dt>**\_ARRAYEQUAL FILTERACTION**</dt> </dl>                  | Indica che il contenuto della matrice è uguale. Il flag deve essere usato con una struttura di **\_ matrice FILTERACTION** .<br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <dt>**\_DEREFPROPERTY FILTERACTION**</dt> </dl>         | Descrive un criterio di corrispondenza in un offset (in byte) dal protocollo.<br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <dt>**FILTERACTION \_ OID \_ contiene**</dt> </dl>           | Valuta una sottostringa all'interno di un identificatore di oggetto. L'azione deve essere utilizzata con la **struttura \_ OID FILTERACTION** .<br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <dt>**l' \_ OID FILTERACTION \_ inizia \_ con**</dt> </dl> | Valuta una sottostringa che inizia un identificatore di oggetto. Il flag deve essere utilizzato con **\_ OID FILTERACTION**.<br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <dt>**l' \_ OID FILTERACTION \_ Termina \_ con**</dt> </dl>       | Valuta una sottostringa che termina un identificatore di oggetto. Il flag deve essere utilizzato con **\_ OID FILTERACTION**.<br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <dt>**\_viti FILTERACTION addr \_**</dt> </dl>                 | Contiene un indirizzo MAC Vine.<br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <dt>**\_espressione FILTERACTION**</dt> </dl>                  | Contiene un'espressione di azione.<br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <dt>**\_bool FILTERACTION**</dt> </dl>                                    | Contiene un tipo di dati **bool** .<br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <dt>**\_direzione filtro \_ Avanti**</dt> </dl>                       | Controlla la direzione sequenziale (frame successivo) all'interno di un file di acquisizione.<br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <dt>**\_direzione filtro \_ precedente**</dt> </dl>                       | Controlla la direzione sequenziale (frame precedente) all'interno di un file di acquisizione.<br/>                                                |



 

</dd> <dt>

**hProperty**
</dt> <dd>

Handle per una chiave della proprietà.

</dd> <dt>

**Valore**
</dt> <dd>

Valore di un oggetto.

</dd> <dt>

**hProtocol**
</dt> <dd>

Handle per visualizzare il protocollo di filtro.

</dd> <dt>

**lpArray**
</dt> <dd>

Puntatore a una matrice.

</dd> <dt>

**lpProtocolTable**
</dt> <dd>

Puntatore a un elenco di protocolli progettato per verificare l'esistenza del protocollo in un frame.

</dd> <dt>

**lpAddress**
</dt> <dd>

Puntatore all'indirizzo del tipo di kernel. Ad esempio, MAC o IP.

</dd> <dt>

**lpLargeInt**
</dt> <dd>

Double **DWORD** usato in un'applicazione Windows NT o Windows 2000.

</dd> <dt>

**lpTime**
</dt> <dd>

Puntatore a una struttura **SYSTEMTIME** .

</dd> <dt>

**lpOID**
</dt> <dd>

Puntatore alla struttura dell' **\_ identificatore di oggetto** (OID).

</dd> <dt>

**ByteCount**
</dt> <dd>

Numero, in byte, nel frame.

</dd> <dt>

**ByteOffset**
</dt> <dd>

Valore byte di offset della struttura FILTEROBJECT utilizzata per confrontare le matrici.

</dd> <dt>

**pNext**
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




