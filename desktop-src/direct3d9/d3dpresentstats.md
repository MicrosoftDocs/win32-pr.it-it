---
description: Descrive le statistiche di presentazione catena relative alle chiamate PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Struttura D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235070"
---
# <a name="d3dpresentstats-structure"></a>Struttura D3DPRESENTSTATS

Descrive le statistiche di presentazione catena relative alle chiamate [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a>Members

<dl> <dt>

**PresentCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Esecuzione del conteggio delle chiamate di presentazione riuscite effettuate da un dispositivo di visualizzazione attualmente in fase di output sullo schermo. Questo parametro è effettivamente l'ID attuale dell'ultima chiamata presente e non è necessariamente il numero totale di chiamate API effettuate.

</dd> <dt>

**PresentRefreshCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Il numero di vblank in corrispondenza del quale l'ultimo presente è stato visualizzato sullo schermo, il numero di vblank viene incrementato una volta ogni intervallo di vblank.

</dd> <dt>

**SyncRefreshCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Il numero di vblank quando l'utilità di pianificazione ha ultimo campionato l'ora del computer chiamando QueryPerformanceCounter.

</dd> <dt>

**SyncQPCTime**
</dt> <dd>

Tipo: **[ **\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Ultimo tempo del computer Campionato dell'utilità di pianificazione, ottenuto chiamando [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).

</dd> <dt>

**SyncGPUTime**
</dt> <dd>

Tipo: **[ **\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando un'applicazione 9Ex adotta la modalità Flip presente (D3DSWAPEFFECT \_ FLIPEX), le applicazioni possono rilevare la rimozione dei frame chiamando GetPresentStatistics in qualsiasi momento. In effetti, è possibile eseguire le operazioni seguenti.

1.  Eseguire il rendering nel buffer nascosto
2.  Chiamata presente
3.  Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante
4.  Esegue il rendering del frame successivo nel buffer nascosto
5.  Chiamata presente
6.  Ripetere i passaggi 4 e 5 1 o più volte
7.  Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante
8.  Confrontare i valori di PresentRefreshCount dalle due strutture D3DPRESENTSTATS archiviate. L'applicazione può calcolare il PresentRefreshCount corrispondente di un determinato parametro PresentCount in base ai presupposti di incremento PresentRefreshCount e assegnazione PresentCount dei presentatori frame. Se l'ultimo esempio di PresentRefreshCount non corrisponde a PresentCount (ad esempio, se il PresentRefreshCount è stato incrementato ma PresentCount non lo è, è stato eliminato il frame).

Le applicazioni possono determinare se un frame è stato eliminato eseguendo il campionamento di due istanze di PresentCount e GetPresentStats (chiamando l'API GetPresentStats in due punti nel tempo). Ad esempio, un'applicazione multimediale che presenta alla stessa frequenza della frequenza di aggiornamento del monitor (ad esempio, la frequenza di aggiornamento del monitoraggio è 60Hz, l'applicazione presenta un frame ogni 1/60 secondi) desidera presentare i frame a, B, C, D, E, ognuno dei quali corrisponde agli ID presenti (PresentCount) 1, 2, 3, 7, 8.

Il codice dell'applicazione ha un aspetto analogo alla sequenza seguente.

1.  Eseguire il rendering del frame a nel buffer nascosto
2.  Chiamata presente, PresentCount = 1
3.  Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante
4.  Eseguire il rendering dei 4 frame successivi, B, C, D, E, rispettivamente
5.  Call present 4 volte, PresentCounts = 2, 3, 7, 8, rispettivamente
6.  Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante
7.  Confrontare i valori di PresentRefreshCount dalle due strutture D3DPRESENTSTATS archiviate. Se la differenza è 2, ovvero sono trascorsi 2 intervalli vblank tra le due chiamate API GetPresentStats, l'ultimo frame presentato dovrebbe essere il frame C. Poiché l'applicazione presenta un intervallo di vblank (la frequenza di aggiornamento del monitoraggio), il tempo trascorso tra il frame A viene presentato e quando viene presentato il frame C dovrebbe essere 2 vblanks.
8.  Confrontare i valori di PresentCount dalle due strutture D3DPRESENTSTATS archiviate. Se il primo PresentCount è 1 (corrispondente al frame A) e il secondo PresentCount è 3 (corrispondente al frame C), non sono stati eliminati frame. Se il secondo PresentCount è 3, che corrisponde al frame D, l'applicazione sa che un frame è stato eliminato.

Si noti che GetPresentStatistics verrà elaborato dopo che è stato chiamato, indipendentemente dallo stato delle chiamate PresentEx in modalità FLIPEX.

**Windows Vista:** Le chiamate attuali verranno accodate e quindi elaborate prima che venga elaborata la chiamata GetPresentStats.

Quando un'applicazione rileva che la presentazione di determinati frame è dietro, può ignorare tali frame e correggere la presentazione per eseguire nuovamente la sincronizzazione con vblank. A tale scopo, un'applicazione non può semplicemente eseguire il rendering dei frame tardivi e avviare il rendering con il frame corretto successivo nella coda. Tuttavia, se un'applicazione ha già avviato il rendering dei frame tardivi, può usare un nuovo parametro presente in D3D9Ex denominato D3DPRESENT \_ FORCEIMMEDIATE. Il flag verrà passato nei parametri della chiamata API presente e indicherà al runtime che il frame verrà elaborato immediatamente entro l'intervallo di vblank successivo, in realtà non visibile sullo schermo. Di seguito è riportato l'esempio di utilizzo dell'applicazione dopo l'ultimo passaggio dell'esempio precedente.

1.  Esegue il rendering del frame successivo nel buffer nascosto
2.  Individuare da PresentRefreshCount che il frame successivo è già in ritardo
3.  Imposta l'intervallo presente su D3DPRESENT \_ FORCEIMMEDIATE
4.  Chiamata presente nel frame successivo

Le applicazioni possono sincronizzare flussi video e audio nello stesso modo, perché il comportamento di GetPresentStatistics non cambia in questo scenario.

La modalità D3D9Ex Flip fornisce informazioni sulle statistiche sui frame per le applicazioni con finestra e le applicazioni 9Ex a schermo intero.

**Windows Vista:** Utilizzare le API di DWM per recuperare le statistiche presenti.

Quando Gestione finestre desktop è disattivato, le applicazioni 9Ex in modalità finestra che usano la modalità Flip riceveranno le informazioni sulle statistiche di accuratezza limitata.

* * Windows Vista: * *

Se un'applicazione non è sufficientemente veloce da soddisfare la frequenza di aggiornamento del monitoraggio, probabilmente a causa di hardware lento o di risorse di sistema insufficienti, è possibile che si verifichi un problema di grafica. Un problema è un singhiozzo visivo così chiamato. Se un monitoraggio è impostato per l'aggiornamento a 60 Hz e l'applicazione può gestire solo 30 fps, la metà dei frame avrà problemi.

Le applicazioni possono rilevare un problema tenendo traccia dei SynchRefreshCount. Ad esempio, un'applicazione potrebbe eseguire la sequenza di azioni seguente.

1.  Eseguire il rendering nel buffer nascosto.
2.  Chiamata presente.
3.  Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante.
4.  Esegue il rendering del frame successivo nel buffer nascosto.
5.  Chiamata presente.
6.  Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante.
7.  Confrontare i valori di SyncRefreshCount dalle due strutture D3DPRESENTSTATS archiviate. Se la differenza è maggiore di uno, un frame è stato ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
