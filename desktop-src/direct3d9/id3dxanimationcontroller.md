---
description: Questa interfaccia viene utilizzata per controllare la funzionalità di animazione, connettendo set di animazioni ai frame di trasformazione che vengono animati.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: Interfaccia ID3DXAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323031"
---
# <a name="id3dxanimationcontroller-interface"></a>Interfaccia ID3DXAnimationController

Questa interfaccia viene utilizzata per controllare la funzionalità di animazione, connettendo set di animazioni ai frame di trasformazione che vengono animati. L'interfaccia dispone di metodi per combinare più animazioni e modificare i parametri di fusione nel tempo per consentire transizioni senza problemi e altri effetti.

## <a name="members"></a>Membri

L'interfaccia **ID3DXAnimationController** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationController** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXAnimationController** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Aggiunge un'animazione alla mesh e sposta in avanti il tempo di animazione globale in base a un importo specificato.<br/>                                                              |
| [**CloneAnimationController**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Clona, o copia, un controller di animazione.<br/>                                                                                                  |
| [**Getanimationt**](id3dxanimationcontroller--getanimationset.md)                     | Ottiene un set di animazioni.<br/>                                                                                                                       |
| [**GetAnimationSetByName**](id3dxanimationcontroller--getanimationsetbyname.md)         | Ottiene un set di animazioni, dato il relativo nome.<br/>                                                                                                       |
| [**GetCurrentPriorityBlend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Restituisce un handle di evento a un evento di combinazione di priorità attualmente in esecuzione.<br/>                                                                 |
| [**GetCurrentTrackEvent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Restituisce un handle di evento per l'evento attualmente in esecuzione sulla traccia di animazione specificata.<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | Ottiene una descrizione di un evento di animazione specificato.<br/>                                                                                           |
| [**GetMaxNumAnimationOutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Ottenere il numero massimo di output di animazione che il controller di animazione può supportare.<br/>                                                            |
| [**GetMaxNumAnimationSets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Ottiene il numero massimo di set di animazioni che il controller di animazione può supportare.<br/>                                                              |
| [**GetMaxNumEvents**](id3dxanimationcontroller--getmaxnumevents.md)                     | Ottiene il numero massimo di eventi che il controller di animazione può supportare.<br/>                                                                      |
| [**GetMaxNumTracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Ottiene il numero massimo di tracce nel controller di animazione.<br/>                                                                               |
| [**GetNumAnimationSets**](id3dxanimationcontroller--getnumanimationsets.md)             | Restituisce il numero di set di animazioni attualmente registrati nel controller di animazione.<br/>                                                       |
| [**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)                   | Ottiene il peso della fusione di priorità corrente utilizzato dal controller di animazione.<br/>                                                                  |
| [**GetTime**](id3dxanimationcontroller--gettime.md)                                     | Ottiene il tempo di animazione globale.<br/>                                                                                                              |
| [**GetTrackAnimationSet**](id3dxanimationcontroller--gettrackanimationset.md)           | Ottiene il set di animazioni per la traccia specificata.<br/>                                                                                                  |
| [**GetTrackDesc**](id3dxanimationcontroller--gettrackdesc.md)                           | Ottiene la descrizione della traccia.<br/>                                                                                                                  |
| [**GetUpcomingPriorityBlend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Restituisce un handle di evento per l'evento di Blend di priorità successivo pianificato per essere eseguito dopo un evento specificato.<br/>                                         |
| [**GetUpcomingTrackEvent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Restituisce un handle di evento all'evento successivo pianificato in modo che venga eseguito dopo un evento specificato in una traccia di animazione.<br/>                                  |
| [**KeyPriorityBlend**](id3dxanimationcontroller--keypriorityblend.md)                   | Imposta la combinazione di chiavi di evento per la traccia di animazione specificata.<br/>                                                                                  |
| [**KeyTrackEnable**](id3dxanimationcontroller--keytrackenable.md)                       | Imposta una chiave evento che Abilita o Disabilita una traccia dell'animazione.<br/>                                                                               |
| [**KeyTrackPosition**](id3dxanimationcontroller--keytrackposition.md)                   | Imposta una chiave evento che modifica l'ora locale di una traccia di animazione.<br/>                                                                         |
| [**KeyTrackSpeed**](id3dxanimationcontroller--keytrackspeed.md)                         | Imposta una chiave evento che modifica la frequenza di riproduzione di una traccia di animazione.<br/>                                                                       |
| [**KeyTrackWeight**](id3dxanimationcontroller--keytrackweight.md)                       | Imposta una chiave evento che modifica il peso di una traccia di animazione. Il peso viene usato come moltiplicatore quando si combinano più tracce.<br/> |
| [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)     | Aggiunge un output di animazione al controller di animazione e registra i puntatori per le trasformazioni di scala, rotazione e conversione (SRT).<br/>          |
| [**RegisterAnimationSet**](id3dxanimationcontroller--registeranimationset.md)           | Aggiunge un set di animazioni al controller dell'animazione.<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | Reimposta il tempo di animazione globale su zero. Tutti gli eventi in sospeso manterranno le pianificazioni originali, ma nel nuovo intervallo di tempo.<br/>                 |
| [**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)                   | Imposta il peso della combinazione di priorità usato dal controller di animazione.<br/>                                                                          |
| [**SetTrackAnimationSet**](id3dxanimationcontroller--settrackanimationset.md)           | Applica il set di animazioni alla traccia specificata.<br/>                                                                                            |
| [**SetTrackDesc**](id3dxanimationcontroller--settrackdesc.md)                           | Imposta la descrizione della traccia.<br/>                                                                                                                  |
| [**SetTrackEnable**](id3dxanimationcontroller--settrackenable.md)                       | Abilita o Disabilita una traccia nel controller animazione.<br/>                                                                                     |
| [**SetTrackPosition**](id3dxanimationcontroller--settrackposition.md)                   | Imposta la traccia sull'ora di animazione locale specificata.<br/>                                                                                        |
| [**SetTrackPriority**](id3dxanimationcontroller--settrackpriority.md)                   | Imposta il peso della combinazione di priorità per la traccia di animazione specificata.<br/>                                                                         |
| [**SetTrackSpeed**](id3dxanimationcontroller--settrackspeed.md)                         | Imposta la velocità della traccia. La velocità della traccia è simile a un moltiplicatore usato per velocizzare o rallentare la riproduzione della traccia.<br/>            |
| [**SetTrackWeight**](id3dxanimationcontroller--settrackweight.md)                       | Imposta il peso della traccia. Il peso viene usato per determinare come unire più tracce.<br/>                                                |
| [**UnkeyAllPriorityBlends**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Rimuove tutti gli eventi di combinazione di priorità pianificati dal controller animazione.<br/>                                                                   |
| [**UnkeyAllTrackEvents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Rimuove tutti gli eventi da una traccia di animazione specificata.<br/>                                                                                         |
| [**UnkeyEvent**](id3dxanimationcontroller--unkeyevent.md)                               | Rimuove un evento specificato da una traccia di animazione, impedendo l'esecuzione dell'evento.<br/>                                                    |
| [**UnregisterAnimationSet**](id3dxanimationcontroller--unregisteranimationset.md)       | Rimuove un set di animazioni dal controller animazione.<br/>                                                                                      |
| [**ValidateEvent**](id3dxanimationcontroller--validateevent.md)                         | Verifica se un handle di evento specificato è valido e se l'evento di animazione non è stato ancora completato.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Creare un oggetto controller di animazione con [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).

Il tipo LPD3DXANIMATIONCONTROLLER è definito come puntatore all'interfaccia **ID3DXAnimationController** .


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



Il tipo D3DXEVENTHANDLE è definito come handle di evento per gli eventi del controller di animazione.


```
typedef DWORD D3DXEVENTHANDLE;
```



Il tipo LPD3DXEVENTHANDLE è definito come puntatore a un handle di evento per gli eventi del controller di animazione.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
