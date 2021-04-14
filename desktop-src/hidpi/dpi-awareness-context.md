---
title: Handle di DPI_AWARENESS_CONTEXT (windef. h)
description: Identifica il contesto di consapevolezza per una finestra.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340752"
---
# <a name="dpi_awareness_context-handle"></a>Handle del contesto di \_ consapevolezza dpi \_

Identifica il contesto di consapevolezza per una finestra.

## <a name="syntax"></a>Sintassi

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Costanti

**contesto di consapevolezza DPI non \_ \_ \_ consapevole**<dl> Valori DPI non compatibili. Questa finestra non viene ridimensionata per le modifiche DPI e si presuppone sempre un fattore di scala pari a 100% (96 DPI). Il sistema verrà ridimensionato automaticamente in base a qualsiasi altra impostazione DPI.  
</dl>

**\_riconoscimento del \_ sistema del contesto \_ \_ di compatibilità dpi**<dl> Compatibile con DPI del sistema. Questa finestra non viene ridimensionata per le modifiche DPI. Eseguirà una query per il valore DPI una volta e utilizzerà tale valore per la durata del processo. Se il valore DPI viene modificato, il processo non si adatterà al nuovo valore DPI. Il valore verrà automaticamente scalato verso l'alto o verso il basso dal sistema in caso di variazione del valore DPI rispetto al valore di sistema.  
</dl>

**\_contesto di consapevolezza dpi \_ \_ per \_ monitoraggio \_**<dl> Per il monitor compatibile con DPI. Questa finestra Controlla il valore DPI quando viene creato e regola il fattore di scala ogni volta che viene modificato il valore DPI. Questi processi non vengono ridimensionati automaticamente dal sistema.  
</dl>

**\_Contesto di riconoscimento dpi \_ \_ per monitoraggio con \_ \_ riconoscimento \_ v2**<dl> Noto anche come **per il monitor V2**. Avanzamento rispetto alla modalità di riconoscimento DPI per monitor originale, che consente alle applicazioni di accedere ai nuovi comportamenti di ridimensionamento correlati a DPI in base a una finestra di primo livello.  
Per monitor V2 è stato reso disponibile nell'aggiornamento dei creatori di Windows 10 e non è disponibile nelle versioni precedenti del sistema operativo.  
I comportamenti aggiuntivi introdotti sono i seguenti:

-   **Notifiche di modifica del valore dpi della finestra figlio** : in per i contesti di monitoraggio V2, l'intero albero della finestra riceve una notifica delle modifiche DPI che si verificano.
-   **Ridimensionamento dell'area non client** : tutte le finestre avranno automaticamente un'area non client disegnata in modo sensibile ai DPI. Le chiamate a [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) non sono necessarie.
-   **Ridimensionamento dei menu Win32** : tutti i menu Ntuser creati nei contesti per monitor V2 verranno ridimensionati in base al monitoraggio.
-   **Ridimensionamento della finestra di dialogo** : le finestre di dialogo Win32 create nei contesti per monitor V2 risponderanno automaticamente alle modifiche DPI.
-   **Miglioramento della scalabilità dei controlli comctl32: i** vari controlli comctl32 hanno migliorato il comportamento di scalabilità dpi in per i contesti di monitoraggio V2.
-   **Miglioramento del comportamento del tema** : gli handle di uxtheme aperti nel contesto di una finestra per monitor V2 funzioneranno in termini di dpi associato a tale finestra.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI non è a conoscenza della migliore qualità del contenuto basato su GDI. Questa modalità si comporta in modo analogo a DPI_AWARENESS_CONTEXT_UNAWARE, ma consente inoltre al sistema di migliorare automaticamente la qualità di rendering del testo e di altre primitive basate su GDI quando la finestra viene visualizzata in un monitor con valori DPI alti.

Per informazioni dettagliate, vedere [miglioramento dell'esperienza con valori DPI elevati nelle app desktop basate su GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED è stato introdotto nell'aggiornamento del 2018 ottobre di Windows 10 (noto anche come versione 1809).


## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----|-----------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1607 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato <br/>  |
| Intestazione<br/>                   | <dl> <dt>windef. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AreDpiAwarenessContextsEqual**](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[**GetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[**GetWindowDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[**IsValidDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
