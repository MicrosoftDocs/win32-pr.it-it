---
title: DPI_AWARENESS_CONTEXT handle (windef.h)
description: Identifica il contesto di riconoscimento per una finestra.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 25e270f59af32b33fdb5ad3f511b693b3eebad71407d48b80a72aff5996edf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727181"
---
# <a name="dpi_awareness_context-handle"></a>Handle DI CONTESTO DI \_ CONSAPEVOLEZZA DPI \_

Identifica il contesto di riconoscimento per una finestra.

## <a name="syntax"></a>Sintassi

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a>Costanti

**CONTESTO DI CONSAPEVOLEZZA DPI \_ \_ \_ INCONSAPEVOLE**<dl> DPI inconsapevole. Questa finestra non viene ridimensionata per le modifiche DPI e si presuppone sempre che abbia un fattore di scala del 100% (96 DPI). Verrà ridimensionata automaticamente dal sistema in qualsiasi altra impostazione DPI.  
</dl>

**RICONOSCIMENTO DEL CONTESTO DI RICONOSCIMENTO DPI \_ \_ \_ \_**<dl> In grado di riconoscere DPI di sistema. Questa finestra non viene ridimensionata per le modifiche DPI. Esegue una query per il valore DPI una sola volta e usa tale valore per la durata del processo. Se il valore DPI viene modificato, il processo non verrà modificato in base al nuovo valore DPI. Verrà ridimensionata automaticamente dal sistema quando il valore DPI cambia rispetto al valore di sistema.  
</dl>

**CONTESTO DI CONSAPEVOLEZZA DPI \_ PER MONITORAGGIO IN GRADO DI \_ \_ \_ \_ RICONOSCERE**<dl> Supporto DPI per ogni monitoraggio. Questa finestra controlla il valore DPI quando viene creato e regola il fattore di scala ogni volta che il valore DPI cambia. Questi processi non vengono ridimensionati automaticamente dal sistema.  
</dl>

**CONTESTO DI RICONOSCIMENTO DPI \_ \_ PER MONITOR AWARE \_ \_ \_ \_ V2**<dl> Nota anche come **Per Monitor v2.** Miglioramento rispetto alla modalità di riconoscimento DPI originale per monitoraggio, che consente alle applicazioni di accedere ai nuovi comportamenti di ridimensionamento correlati a DPI in base alla finestra di primo livello.  
Per Monitor v2 è stato reso disponibile nell'aggiornamento creators di Windows 10 e non è disponibile nelle versioni precedenti del sistema operativo.  
I comportamenti aggiuntivi introdotti sono i seguenti:

-   **Notifiche di modifica DPI** della finestra figlio: nei contesti Per monitoraggio v2, l'intero albero della finestra viene notificato di eventuali modifiche DPI che si verificano.
-   **Ridimensionamento dell'area non client:** tutte le finestre avranno automaticamente l'area non client disegnata in modo sensibile al valore DPI. Le chiamate [**a EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) non sono necessarie.
-   **Ridimensionamento dei menu Win32:** tutti i menu NTUSER creati nei contesti Per monitoraggio v2 verranno ridimensionati in base al monitoraggio.
-   **Ridimensionamento delle** finestre di dialogo: le finestre di dialogo Win32 create nei contesti Per monitoraggio v2 risponderanno automaticamente alle modifiche DPI.
-   **Ridimensionamento migliorato dei controlli comctl32:** vari controlli comctl32 hanno migliorato il comportamento di ridimensionamento DPI nei contesti Per Monitor v2.
-   **Miglioramento del comportamento di** uxtheme: gli handle UxTheme aperti nel contesto di una finestra per monitoraggio v2 funzioneranno in termini di DPI associato a tale finestra.

  
</dl>

**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**

DPI inconsapevole della qualità migliorata del contenuto basato su GDI. Questa modalità si comporta in modo analogo a DPI_AWARENESS_CONTEXT_UNAWARE, ma consente anche al sistema di migliorare automaticamente la qualità di rendering del testo e di altre primitive basate su GDI quando la finestra viene visualizzata su un monitor con valori DPI elevati.

Per altre informazioni, vedere [Miglioramento dell'esperienza DPI elevata nelle app desktop basate su GDI.](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97)

DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED è stato introdotto nell'aggiornamento di ottobre 2018 di Windows 10 (nota anche come versione 1809).


## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|----|-----------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1607 \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato <br/>  |
| Intestazione<br/>                   | <dl> <dt>windef.h</dt> </dl> |

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
