---
title: Considerazioni sulle prestazioni e procedure consigliate
description: Questo argomento presenta un set di procedure consigliate per l'uso delle API Gestione finestre desktop (DWM).
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Gestione finestre desktop (DWM), procedure consigliate
- DWM (Gestione finestre desktop),procedure consigliate
- Gestione finestre desktop (DWM), procedure per le applicazioni
- DWM (Gestione finestre desktop),procedure per le applicazioni
- Gestione finestre desktop (DWM), procedure di disegno
- DWM (Gestione finestre desktop),procedure di disegno
- Gestione finestre desktop (DWM), sfocatura dietro l'effetto
- Effetto DWM (Gestione finestre desktop),sfocatura dietro
- procedure per l'applicazione
- procedure di disegno
- effetto sfocatura dietro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7affbbf5ebca91a4e5172e75f88da4b9fe8e33f6e1e3de1e7a735add816a313f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280274"
---
# <a name="performance-considerations-and-best-practices"></a>Considerazioni sulle prestazioni e procedure consigliate

Questo argomento presenta un set di procedure consigliate per l'uso delle API Gestione finestre desktop (DWM).

In questo argomento sono incluse le sezioni seguenti:

-   [Procedure applicative per DWM](#application-practices-for-dwm)
-   [Procedure di disegno per DWM](#drawing-practices-for-dwm)
-   [Area client Blur-Behind DWM](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Procedure applicative per DWM

Se l'applicazione gestisce il ridimensionamento di punti per pollice (dpi), è possibile dichiarare un'applicazione come con riconoscimento dpi e impedire il ridimensionamento automatico impostando il flag con riconoscimento dpi nel manifesto del programma o chiamando la [**funzione SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) durante l'inizializzazione del programma.

Con la composizione DWM attivata, le applicazioni nascosti non ricevono più messaggi [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) e non viene richiesto di eseguire di nuovo il rendering. Il contenuto di ogni finestra è già disponibile per comporre l'immagine della schermata.

Le finestre [**WS \_ EX \_ TRANSPARENT**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) di primo livello devono essere combinate con uno **stile WS \_ EX \_** a livelli ai fini dell'hit testing. **WS \_ EX \_ TRANSPARENT** nel senso classico, senza reindirizzamento, è utile per le finestre figlio in una gerarchia di finestre che appartengono allo stesso thread, ma non sono destinate alle finestre di primo livello.

Usare aree o livelli per creare finestre modellate o miste. Si noti che in Windows Vista e versioni successive di Windows, il disegno personalizzato solo parte di una finestra di primo livello non fornirà il contenuto non aggiornate desiderato nelle aree non disegnate.

È possibile usare API come [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) per determinare determinati valori effettivi. Se si dispone di un contesto di dispositivo (DC) per una finestra reindirizzata, l'origine restituita da **GetDCOrgEx** non corrisponderà all'origine della finestra sullo schermo. L'origine sarà invece l'origine della superficie del buffer nascosto per la finestra: (0, 0).

Quando tutto il resto ha esito negativo, disabilitare il rendering della finestra [**chiamando la funzione DwmSetWindowAttribute.**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute)

## <a name="drawing-practices-for-dwm"></a>Procedure di disegno per DWM

Evitare di disegnare direttamente sulla superficie di visualizzazione principale. In questo modo DWM verrà forzato a disabilitare la composizione fino a quando l'applicazione non rilascia la superficie del dispositivo principale.

Valutare se l'applicazione deve fornire il proprio doppio buffer. DWM raddoppia in modo efficace il contenuto e presenta la finestra in un singolo frame.

Evitare la lettura o la scrittura in un controller di dominio di visualizzazione. Anche se supportato da DWM, non è consigliabile a causa della riduzione delle prestazioni.

Evitare di disegnare nell'area non client. Anche se quest'area è accessibile dall'applicazione e il disegno è supportato dall'API Win32 Microsoft, questa operazione può causare la perdita di qualsiasi bordo di cristallo della finestra.

Evitare di combinare Windows Graphics Device Interface (GDI) e Microsoft DirectX a meno che non si sovrappongano. Se è necessaria la combinazione, disegnare il contenuto GDI in una superficie software DirectX e combinarli prima della composizione sullo schermo oppure disegnarli in finestre separate.

Usare [**la funzione BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) [**o StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) Windows GDI+ presentare il disegno per il rendering. GDI+ esegue il rendering di una linea di analisi alla volta con il rendering del software. Ciò può causare sfarfallio nelle applicazioni.

## <a name="dwm-blur-behind-client-region"></a>Area client Blur-Behind DWM

Il rendering dell'effetto blur-behind è un'operazione a elevato utilizzo di risorse sia per la CPU che per l'unità di elaborazione grafica (GPU). Agli sviluppatori di applicazioni viene chiesto di considerare le implicazioni dell'uso della sfocatura dell'area client in modo che non utilizzi un numero eccessivo di risorse. È necessario prestare particolare attenzione nei casi seguenti:

-   Quando si prevede che le dimensioni della sfocatura dell'area client siano significative, anche se non verranno eseguiti aggiornamenti nell'area sfocata stessa. È necessario eseguire il rendering della sfocatura nel caso in cui si verifichino aggiornamenti nell'area sfocata della finestra, che comporta costi di CPU e GPU. Inoltre, le operazioni della finestra (spostamento/ridimensionamento/transizioni) comportano costi maggiori.
-   Quando si prevedono aggiornamenti significativi nell'area client sfocata. In questo modo sarà necessario ridisegnare la sfocatura a ogni aggiornamento e utilizzare un numero eccessivo di risorse.
-   Se si prevede che la sfocatura copre un'area significativa e sono previsti anche aggiornamenti a tale area, è consigliabile non sfocare l'area client.

 

 