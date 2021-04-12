---
description: Enumerazione utilizzata per indicare il tipo di un evento.
MS-HAID: vspixengine.EVENTTYPE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione EVENTTYPE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7A6F396-5BC0-4963-ABFD-ACB7AAE475F5
api_name:
- EVENTTYPE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 60af0090e440cd101211394cff98c9d9a501f4ba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401176"
---
# <a name="span-idvspixengineeventtypespaneventtype-enumeration"></a><span id="vspixengine.eventtype"></span>Enumerazione EVENTTYPE

Enumerazione utilizzata per indicare il tipo di un evento.

## <a name="syntax"></a>Sintassi

```cpp
C++ 
enum EVENTTYPE {
  ET_NONE = 0, 
  ET_SESSIONSTART, 
  ET_SESSIONEND, 
  ET_PROCESSSTART, 
  ET_PROCESSEND, 
  ET_FRAMEBEGIN, 
  ET_FRAMEEND, 
  ET_USEREVENTBEGIN, 
  ET_USEREVENTEND, 
  ET_USERMARKER, 
  ET_CALL, 
  ET_OBJECTCREATION, 
  ET_OBJECTPOPULATION, 
  ET_CALLSYNC, 
  ET_DRAW, 
  ET_DISPATCH 
};
```

## <a name="constants"></a>Costanti

<span id="ET_NONE"></span><span id="et_none"></span>**ET \_ None**  
Valore che corrisponde a nessun evento.

<span id="ET_SESSIONSTART"></span><span id="et_sessionstart"></span>**\_SESSIONSTART et**  
Valore che corrisponde a un evento di avvio della sessione.

<span id="ET_SESSIONEND"></span><span id="et_sessionend"></span>**\_SESSIONEND et**  
Valore che corrisponde a un evento di fine sessione.

<span id="ET_PROCESSSTART"></span><span id="et_processstart"></span>**\_PROCESSSTART et**  
Valore che corrisponde a un evento di avvio del processo.

<span id="ET_PROCESSEND"></span><span id="et_processend"></span>**\_PROCESSEND et**  
Valore che corrisponde a un evento di fine del processo.

<span id="ET_FRAMEBEGIN"></span><span id="et_framebegin"></span>**\_FRAMEBEGIN et**  
Valore che corrisponde a un evento di inizio frame.

<span id="ET_FRAMEEND"></span><span id="et_frameend"></span>**\_FRAMEEND et**  
Valore che corrisponde a un evento di fine frame. Non usato.

<span id="ET_USEREVENTBEGIN"></span><span id="et_usereventbegin"></span>**\_USEREVENTBEGIN et**  
Valore che corrisponde a un evento di inizio evento utente.

<span id="ET_USEREVENTEND"></span><span id="et_usereventend"></span>**\_USEREVENTEND et**  
Valore che corrisponde a un evento di fine evento utente. Non usato.

<span id="ET_USERMARKER"></span><span id="et_usermarker"></span>**\_USERMARKER et**  
Valore che corrisponde a un evento dell'indicatore utente.

<span id="ET_CALL"></span><span id="et_call"></span>**chiamata a ET \_**  
Valore che corrisponde a un evento di chiamata.

<span id="ET_OBJECTCREATION"></span><span id="et_objectcreation"></span>**\_OBJECTCREATION et**  
Valore che corrisponde a un evento di creazione di un oggetto.

<span id="ET_OBJECTPOPULATION"></span><span id="et_objectpopulation"></span>**\_OBJECTPOPULATION et**  
Valore che corrisponde a un evento di popolamento dell'oggetto.

<span id="ET_CALLSYNC"></span><span id="et_callsync"></span>**\_CALLSYNC et**  

<span id="ET_DRAW"></span><span id="et_draw"></span>**\_disegni et**  
Valore che corrisponde a un evento di chiamata di progetto.

<span id="ET_DISPATCH"></span><span id="et_dispatch"></span>**invio di ET \_**  
Valore che corrisponde a un evento dispatch.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>
