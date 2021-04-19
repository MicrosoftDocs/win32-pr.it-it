---
description: Contiene gli attributi di condivisione DDE gestiti da NetDDE Share database Manager (DSDM).
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: Struttura NDDESHAREINFO (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317315"
---
# <a name="nddeshareinfo-structure"></a>Struttura NDDESHAREINFO

\[Il DDE di rete non è più supportato. Nddeapi.dll è presente in Windows Vista, ma tutte le chiamate di funzione restituiscono NDDE \_ non \_ implementate.\]

Contiene gli attributi di condivisione DDE gestiti da NetDDE Share database Manager (DSDM). Il descrittore di sicurezza associato a ogni condivisione DDE non viene passato tramite questa struttura, ma è possibile accedervi tramite funzioni specifiche. L'API DSDM di NetDDE accetta questa struttura per le funzioni set; per le funzioni Get, DSDM restituisce la struttura compressa nel buffer fornito insieme ai dati a cui fanno riferimento i membri **lpszShareName**, **lpszAppTopicList** e **lpszItemList**.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**lRevision**
</dt> <dd>

Livello di revisione della struttura **NDDESHAREINFO** . Attualmente, il livello di revisione è 1.

</dd> <dt>

**lpszShareName**
</dt> <dd>

Nome della condivisione. La lunghezza della stringa non deve superare il numero massimo di \_ caratteri NDDESHARENAME.

</dd> <dt>

**lShareType**
</dt> <dd>

Uno o più tipi di condivisione DDE. Questo membro può essere una combinazione dei seguenti tipi di condivisione DDE supportati.



| Tipo di condivisione                                                                                                                                                                                                                           | Significato                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <dt>**Condividi \_ Digitare \_ New**</dt> <dt>0x02</dt> </dl>          | La condivisione contiene una coppia applicazione/argomento OLE.<br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <dt>**Condividi \_ Digitare \_**</dt> <dt>0x01</dt> precedente </dl>          | La condivisione contiene una coppia applicazione/argomento DDE.<br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <dt>**Condividi \_ Digitare \_**</dt> <dt>0x04</dt> statico </dl> | La condivisione contiene una coppia applicazione/argomento statica.<br/> |



 

</dd> <dt>

**lpszAppTopicList**
</dt> <dd>

Puntatore a un buffer contenente stringhe con terminazione null per le coppie di applicazione/argomento DDE, OLE e statiche. Il buffer deve avere il formato seguente:

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

**fSharedFlag**
</dt> <dd>

Se questo membro è **false**, la condivisione DDE non consentirà agli utenti remoti di comunicare tramite DDE tramite DDE. Tuttavia, gli utenti locali possono comunque comunicare tramite la condivisione DDE. I collegamenti client locali sono sempre impliciti se l'elenco DACL associato concede l'accesso.

</dd> <dt>

**fService**
</dt> <dd>

Se questo membro è impostato, la condivisione DDE non verificherà se l'utente corrente lo ha impostato come attendibile prima di consentire la comunicazione DDE.

</dd> <dt>

**fStartAppFlag**
</dt> <dd>

Se questo membro è impostato e la condivisione è attendibile per avviare le applicazioni, NetDDE tenterà di avviare l'applicazione specificata da **lpszAppTopicList** se non è possibile avviare inizialmente una conversazione DDE con l'applicazione.

</dd> <dt>

**nCmdShow**
</dt> <dd>

Quando NetDDE avvia un'applicazione per avviare una conversazione DDE, questo valore viene inviato all'applicazione tramite il parametro *nCmdShow* della funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) . Definisce la modalità preferita per la finestra dell'applicazione da visualizzare in. Questo parametro è significativo solo se **fStartAppFlag** è attivo. L'utente connesso nel cui contesto viene avviata l'applicazione può anche eseguire l'override di questa opzione quando si innalza di livello la condivisione allo stato attendibile. Il valore predefinito per questo membro è SW \_ SHOWMAXIMIZED.

</dd> <dt>

**qModifyId**
</dt> <dd>

Numero di serie a 8 byte che indica il numero di serie della modifica della condivisione DDE. Ogni volta che la condivisione DDE viene modificata da una chiamata a [**NDdeShareSetInfo**](nddesharesetinfo.md) o [**NDdeSetShareSecurity**](nddesetsharesecurity.md) , questi valori vengono modificati.

</dd> <dt>

**cNumItems**
</dt> <dd>

Numero di elementi elencati in **lpszItemList**. Se **cNumItems** è zero, **lpszItemList** è vuoto e le informazioni sulla condivisione e il descrittore di sicurezza associato si applicano a tutti gli elementi serviti dall'applicazione associata.

</dd> <dt>

**lpszItemList**
</dt> <dd>

Puntatore a un buffer contenente stringhe con terminazione null che specificano gli elementi in cui l'applicazione client in una transazione DDE può richiedere o avviare i cicli di notifica. Se non sono elencati elementi, la condivisione DDE consente l'utilizzo di qualsiasi elemento. Il numero di elementi nell'elenco deve corrispondere al numero di **cNumItems** .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Dynamic Data Exchange di rete](network-dynamic-data-exchange.md)
</dt> <dt>

[Strutture DDE di rete](network-dde-structures.md)
</dt> <dt>

[**NDdeSetShareSecurity**](nddesetsharesecurity.md)
</dt> <dt>

[**NDdeShareSetInfo**](nddesharesetinfo.md)
</dt> <dt>

[**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

