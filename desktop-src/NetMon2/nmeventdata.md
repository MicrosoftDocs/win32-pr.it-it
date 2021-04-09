---
description: La struttura NMEVENTDATA contiene informazioni su una condizione dell'evento che viene passata a Network Monitor per inserire una riga nel Visualizzatore esperti.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Struttura NMEVENTDATA (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879674"
---
# <a name="nmeventdata-structure"></a>Struttura NMEVENTDATA

La struttura **NMEVENTDATA** contiene informazioni su una condizione dell'evento che viene passata a Network Monitor per inserire una riga nel Visualizzatore esperti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Numero di versione della struttura **NMEVENTDATA** . Il numero di versione deve essere zero. Le versioni future di Network Monitor possono supportare un numero di versione superiore.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificatore dell'evento. **EventIdent** è univoco per ogni esperto e fa riferimento a una [pagina di riferimento](event-reference-page.md)a un evento.

</dd> <dt>

**Flag**
</dt> <dd>

Set di flag che descrive chi invia i dati dell'evento e come viene visualizzato l'evento.



| Valore                                                                                                                                                                                                                                              | Significato                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**\_esperto flag di evento \_**</dt> </dl>                                                                         | L'evento proviene da un esperto. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ visualizzano la \_ gravità**</dt> </dl>                 | Non visualizzare il livello di gravità per l'evento. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ Visualizza l' \_ origine**</dt> </dl>                       | Non visualizzare il nome dell'origine per l'evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ Visualizza il \_ nome dell'evento \_**</dt> </dl>          | Non visualizzare il nome dell'evento. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ Visualizza la \_ Descrizione**</dt> </dl>        | Non visualizzare la descrizione dell'evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ Visualizza il \_ computer**</dt> </dl>                    | Non visualizzare il nome del computer per l'evento. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ Visualizza l' \_ ora**</dt> </dl>                             | Non visualizzare l'ora dell'evento <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ \_ non \_ Visualizza \_ colonne fisse \_**</dt> </dl> | Non visualizzare la gravità, l'origine, il nome dell'evento, la descrizione, il computer o le colonne temporali. Non si tratta di un flag singolo, ma è un'Unione dei sei flag precedenti. <br/> |



 

</dd> <dt>

**Gravità**
</dt> <dd>

Livello di gravità dell'evento. Il livello di gravità può avere uno dei valori seguenti:

gravità \_ NMEVENT \_ Informational NMEVENT \_ \_ avviso NMEVENT gravità \_ \_ \_ grave avviso NMEVENT \_ gravità \_ errore NMEVENT \_ gravità grave errore NMEVENT gravità \_ \_ \_ \_ errore critico \_

</dd> <dt>

**NumColumns**
</dt> <dd>

Numero di colonne designate nella struttura corrente.

</dd> <dt>

**szSourceName**
</dt> <dd>

Nome dell'esperto visualizzato.

</dd> <dt>

**szEventName**
</dt> <dd>

Nome dell'evento visualizzato.

</dd> <dt>

**szDescription**
</dt> <dd>

Descrizione dell'evento visualizzato.

</dd> <dt>

**szMachine**
</dt> <dd>

Obsoleto, deve essere **null**.

</dd> <dt>

**Giustificazione**
</dt> <dd>

Informazioni visualizzate nella seconda finestra del Visualizzatore eventi. Il membro **giustificazione** può essere **null**. Se è **null**, la seconda finestra non è visibile.

</dd> <dt>

**szUrl**
</dt> <dd>

Riservati Questo membro deve essere **null**.

</dd> <dt>

**SysTime**
</dt> <dd>

Ora in cui si verifica la condizione dell'evento. Il tempo viene misurato in relazione all'inizio dell'acquisizione.

</dd> <dt>

**Colonna**
</dt> <dd>

Tabella delle strutture di colonna visualizzata nel riquadro superiore del Visualizzatore eventi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




