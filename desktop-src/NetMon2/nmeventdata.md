---
description: La struttura NMEVENTDATA contiene informazioni su una condizione dell'evento che viene passata Network Monitor per inserire una riga nel visualizzatore esperti.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Struttura NMEVENTDATA (Netmon.h)
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
ms.openlocfilehash: af2a4775be7d9e123974fbab865a8171d9bc9dec7dacae7692054bc6db0d3085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037041"
---
# <a name="nmeventdata-structure"></a>Struttura NMEVENTDATA

La **struttura NMEVENTDATA** contiene informazioni su una condizione dell'evento che viene passata Network Monitor per inserire una riga nel visualizzatore esperti.

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

**Version**
</dt> <dd>

Numero di versione della **struttura NMEVENTDATA.** Il numero di versione deve essere zero. Le versioni future Network Monitor possono supportare un numero di versione superiore.

</dd> <dt>

**EventIdent**
</dt> <dd>

Identificatore dell'evento. **EventIdent è univoco** per ogni esperto e fa riferimento a una [pagina di riferimento all'evento](event-reference-page.md).

</dd> <dt>

**Flag**
</dt> <dd>

Set di flag che descrive chi invia i dati dell'evento e come viene visualizzato l'evento.



| Valore                                                                                                                                                                                                                                              | Significato                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <dt>**ESPERTO \_ DI FLAG \_ DI EVENTI**</dt> </dl>                                                                         | L'evento è stato generato da un esperto. <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <dt>**NMEVENTFLAG \_ NON VISUALIZZA LA \_ \_ \_ GRAVITÀ**</dt> </dl>                 | Non visualizzare il livello di gravità per l'evento. <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <dt>**NMEVENTFLAG \_ NON \_ VISUALIZZA \_ \_ L'ORIGINE**</dt> </dl>                       | Non visualizzare il nome dell'origine per l'evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <dt>**NMEVENTFLAG \_ NON VISUALIZZA IL NOME \_ \_ \_ \_ DELL'EVENTO**</dt> </dl>          | Non visualizzare il nome dell'evento. <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <dt>**NMEVENTFLAG \_ NON VISUALIZZA LA \_ \_ \_ DESCRIZIONE**</dt> </dl>        | Non visualizzare la descrizione dell'evento. <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <dt>**NMEVENTFLAG \_ NON \_ VISUALIZZA \_ COMPUTER \_**</dt> </dl>                    | Non visualizzare il nome del computer per l'evento. <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <dt>**NMEVENTFLAG \_ NON \_ VISUALIZZA \_ \_ L'ORA**</dt> </dl>                             | Non visualizzare l'ora dell'evento <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <dt>**NMEVENTFLAG \_ NON VISUALIZZA COLONNE \_ \_ \_ \_ FISSE**</dt> </dl> | Non visualizzare le colonne Gravità, Origine, Nome evento, Descrizione, Computer o Ora. Non si tratta di un singolo flag, ma è un'unione dei sei flag precedenti. <br/> |



 

</dd> <dt>

**Gravità**
</dt> <dd>

Livello di gravità dell'evento. Il livello di gravità può avere uno dei valori seguenti:

NMEVENT \_ SEVERITY \_ INFORMATIONAL NMEVENT \_ SEVERITY \_ WARNING NMEVENT \_ SEVERITY \_ STRONG \_ WARNING NMEVENT \_ SEVERITY \_ ERROR NMEVENT \_ SEVERITY \_ SEVERE \_ ERROR NMEVENT \_ SEVERITY \_ CRITICAL \_ ERROR

</dd> <dt>

**Numcolumns**
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

Obsoleto, deve essere **NULL.**

</dd> <dt>

**Giustificazione**
</dt> <dd>

Informazioni visualizzate nella seconda finestra del Visualizzatore eventi. Il **membro Di giustificazione** può essere **NULL.** Se è **NULL,** la seconda finestra non è visibile.

</dd> <dt>

**szUrl**
</dt> <dd>

Riservato; questo membro deve essere **NULL.**

</dd> <dt>

**SysTime**
</dt> <dd>

Ora in cui si verifica la condizione dell'evento. Il tempo viene misurato rispetto all'inizio dell'acquisizione.

</dd> <dt>

**Colonna**
</dt> <dd>

Tabella delle strutture delle colonne visualizzata nel riquadro superiore della Visualizzatore eventi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




