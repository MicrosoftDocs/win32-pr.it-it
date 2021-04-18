---
title: Considerazioni sulle prestazioni e procedure consigliate
description: In questo argomento viene presentata una serie di procedure consigliate per l'utilizzo delle API di Gestione finestre desktop (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Gestione finestre desktop (DWM), procedure consigliate
- DWM (Gestione finestre desktop), procedure consigliate
- Gestione finestre desktop (DWM), procedure per le applicazioni
- DWM (Gestione finestre desktop), procedure per le applicazioni
- Gestione finestre desktop (DWM), procedure di disegno
- DWM (Gestione finestre desktop), procedure di disegno
- Gestione finestre desktop (DWM), effetto sfocatura dietro
- DWM (Gestione finestre desktop), effetto sfocatura dietro
- procedure per le applicazioni
- procedure di disegno
- effetto sfocatura dietro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec76a4920a91f9502940e866d58641a2550d9354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300258"
---
# <a name="performance-considerations-and-best-practices"></a>Considerazioni sulle prestazioni e procedure consigliate

In questo argomento viene presentata una serie di procedure consigliate per l'utilizzo delle API di Gestione finestre desktop (DWM).

In questo argomento sono incluse le sezioni seguenti:

-   [Procedure per le applicazioni per DWM](#application-practices-for-dwm)
-   [Procedure di disegno per DWM](#drawing-practices-for-dwm)
-   [DWM Blur-Behind area client](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Procedure per le applicazioni per DWM

Se l'applicazione gestisce il ridimensionamento DPI (punti per pollice), è possibile dichiarare un'applicazione come compatibile con dpi ed evitare la scalabilità automatica impostando il flag in grado di riconoscere DPI nel manifesto del programma o chiamando la funzione [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) durante l'inizializzazione del programma.

Con la composizione DWM attivata, le applicazioni nascoste non ricevono più messaggi di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) e non viene richiesto di eseguire nuovamente il rendering. Il contenuto di ogni finestra è già disponibile per comporre l'immagine dello schermo.

Le finestre di primo livello [**WS- \_ \_ Transparent**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) devono essere combinate con uno stile **WS \_ ex a \_ livelli** ai fini dell'hit test. **WS \_ Il \_ fatto che, a differenza di quanto** avviene per le finestre figlio in una gerarchia di finestre appartenenti allo stesso thread, non è progettato per le finestre di primo livello.

Usare aree o livelli per creare finestre con forma o con Blend. Si noti che in Windows Vista e nelle versioni successive di Windows, il disegno personalizzato solo parte di una finestra di primo livello non fornirà il contenuto non aggiornato desiderato nelle aree non disegnate.

Le API come [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) possono essere usate per determinare determinati valori effettivi. Se si dispone di un contesto di dispositivo (DC) per una finestra reindirizzata, l'origine restituita da **GetDCOrgEx** non corrisponderà all'origine della finestra sullo schermo. L'origine sarà invece l'origine della superficie del buffer di sfondo per la finestra: (0, 0).

Quando l'operazione ha esito negativo, disabilitare il rendering della finestra chiamando la funzione [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) .

## <a name="drawing-practices-for-dwm"></a>Procedure di disegno per DWM

Evitare di disegnare direttamente nella superficie di visualizzazione principale. In questo modo, la soluzione DWM verrà forzata per disabilitare la composizione fino a quando l'applicazione non rilascia la superficie del dispositivo primario.

Valutare se l'applicazione deve fornire il proprio doppio buffer. DWM raddoppia efficacemente il contenuto e visualizza la finestra in un singolo frame.

Evitare di leggere o scrivere in un controller di dominio di visualizzazione. Sebbene supportato da DWM, questo non è consigliato a causa di una riduzione delle prestazioni.

Evitare di disegnare nell'area non client. Sebbene sia possibile accedere a questa area dall'applicazione e che il disegno sia supportato dall'API Microsoft Win32, questa operazione può causare la perdita di tutti i bordi vetro della finestra.

Evitare di combinare Windows Graphics Device Interface (GDI) e Microsoft DirectX a meno che non si sovrappongano. Se la combinazione è necessaria, è possibile creare il contenuto GDI in una superficie software DirectX e combinarli prima della composizione sullo schermo, altrimenti è possibile crearli in finestre separate.

Utilizzare la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) o [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) anziché GDI+ per presentare il disegno per il rendering. GDI+ esegue il rendering di una riga di analisi alla volta con il rendering software. Questo può causare lo sfarfallio delle applicazioni.

## <a name="dwm-blur-behind-client-region"></a>DWM Blur-Behind area client

Il rendering dell'effetto sfocatura è un'operazione a elevato utilizzo di risorse per la CPU e la GPU (Graphics Processing Unit). Gli sviluppatori di applicazioni sono invitati a prendere in considerazione le implicazioni dell'uso della sfocatura dell'area client in modo che non utilizzi risorse eccessive. È necessario prestare particolare attenzione nei casi seguenti:

-   Quando si prevede che le dimensioni della sfocatura dell'area client siano significative, anche se non si verificheranno aggiornamenti nell'area sfocata. È necessario eseguire il rendering della sfocatura nel caso in cui si verifichino aggiornamenti nell'area sfocata della finestra, che comporta costi CPU e GPU. Inoltre, le operazioni della finestra sulla finestra (spostamento/ridimensionamento/transizioni) comporteranno un numero maggiore di costi.
-   Quando si prevede aggiornamenti significativi nell'area client sfocata. Questa operazione richiederà un ridisegno della sfocatura per ogni aggiornamento e utilizzerà risorse eccessive.
-   Se si prevede che la sfocatura copra un'area significativa ed è previsto anche l'aggiornamento a tale area, si consiglia vivamente di non sfocare l'area client.

 

 