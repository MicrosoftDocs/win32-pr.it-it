---
title: Informazioni sulle icone
description: In questo argomento vengono illustrate le icone.
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- risorse, icone
- icone, aree sensibili
- icone, standard
- Icone standard
- icone, personalizzate
- icone personalizzate
- icone, dimensioni
- creazione di icone
- icone, visualizzazione
- icone, distruzione
- icone, duplicazione
- icone, creazione
- visualizzazione di icone
- eliminazione di icone
- duplicazione delle icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bda00540d613b6d0efd4a080251ebd6407560ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337302"
---
# <a name="about-icons"></a>Informazioni sulle icone

Il sistema utilizza le icone nell'interfaccia utente per rappresentare oggetti quali file, cartelle, collegamenti, applicazioni e documenti. Le funzioni icona consentono alle applicazioni di creare, caricare, visualizzare, disporre, animare ed eliminare le icone. Per informazioni sulla specifica delle icone per i tipi di file, vedere [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).

In questa panoramica vengono fornite informazioni sui seguenti argomenti:

-   [Icona sensibile](#icon-hot-spot)
-   [Tipi di icone](#icon-types)
-   [Dimensioni delle icone](#icon-sizes)
    -   [Per modificare le dimensioni dell'icona di sistema Small](#to-change-the-size-of-the-system-small-icon)
    -   [Per recuperare le dimensioni dell'icona di sistema Small](#to-retrieve-the-size-of-the-system-small-icon)
    -   [Per recuperare le dimensioni dell'icona di sistema large](#to-retrieve-the-size-of-the-system-large-icon)
    -   [Per recuperare le dimensioni dell'icona della shell Small](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [Per modificare le dimensioni dell'icona grande](#to-change-the-size-of-the-large-icon)
    -   [Per recuperare la dimensione dell'icona della shell grande](#to-retrieve-the-size-of-the-shell-large-icon)
-   [Creazione di icone](#icon-creation)
-   [Visualizzazione icona](#icon-display)
-   [Icona di distruzione](#icon-destruction)
-   [Duplicazione delle icone](#icon-duplication)

## <a name="icon-hot-spot"></a>Icona sensibile

Uno dei pixel in un'icona viene designato come area [sensibile, ovvero](#icon-hot-spot)il punto in cui il sistema tiene traccia e riconosce come posizione dell'icona. L'area sensibile di un'icona è in genere il pixel che si trova al centro dell'icona. Se si usa la funzione [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) per creare un'icona, è possibile specificare qualsiasi pixel come area sensibile.

## <a name="icon-types"></a>Tipi di icone

Il sistema operativo fornisce un set di *icone standard* disponibili per qualsiasi applicazione da usare in qualsiasi momento. I file di intestazione Software Development Kit (SDK) contengono gli identificatori per le icone standard, mentre gli identificatori iniziano con il prefisso **Idi \_** .

A ogni icona standard è associata un'immagine predefinita corrispondente. L'utente può sostituire l'immagine predefinita associata a qualsiasi cursore standard in qualsiasi momento.

Le *icone personalizzate* sono progettate per essere utilizzate in un'applicazione specifica e possono essere qualsiasi progettazione. Di seguito sono riportate diverse icone personalizzate.

![diverse icone personalizzate](images/csicn-02.png)

## <a name="icon-sizes"></a>Dimensioni delle icone

Il sistema utilizza quattro dimensioni delle icone:

-   Sistema Small
-   Sistema di grandi dimensioni
-   Shell Small
-   Shell grande

L' *icona di sistema Small* viene visualizzata nella didascalia della finestra.

### <a name="to-change-the-size-of-the-system-small-icon"></a>Per modificare le dimensioni dell'icona di sistema Small

1.  Nel pannello di controllo fare clic su **Visualizza**, quindi sulla scheda **aspetto** .
2.  Selezionare i **pulsanti didascalia** dall'elenco **elemento** , quindi impostare il campo **dimensioni** .

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>Per recuperare le dimensioni dell'icona di sistema Small

-   Chiamare la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ CXSMICON** e **SM \_ CYSMICON**.

L' *icona di sistema grande* viene utilizzata principalmente dalle applicazioni, ma viene visualizzata anche nella finestra di dialogo ALT + TAB. Le funzioni [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona), [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona), [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)e [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) usano tutte le icone di sistema di grandi dimensioni. La dimensione dell'icona di sistema grande è definita dal driver video, pertanto non può essere modificata.

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>Per recuperare le dimensioni dell'icona di sistema large

-   Chiamare [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con **SM \_ CXICON** e **SM \_ CYICON**.

È possibile usare le funzioni [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon), [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)e [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) per lavorare con icone in dimensioni diverse dal sistema di grandi dimensioni.

L' *icona shell Small* viene utilizzata in Esplora risorse e nelle finestre di dialogo comuni. Attualmente, per impostazione predefinita il sistema è di dimensioni ridotte.

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>Per recuperare le dimensioni dell'icona della shell Small

1.  Utilizzare la funzione [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) con `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` per recuperare un handle per l'elenco di immagini di sistema.
2.  Chiamare quindi la funzione [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) per ottenere le dimensioni dell'icona.

L'icona shell grande viene usata sul desktop.

### <a name="to-change-the-size-of-the-large-icon"></a>Per modificare le dimensioni dell'icona grande

1.  Nel pannello di controllo fare clic su **Visualizza**, quindi sulla scheda **aspetto** .
2.  Selezionare l' **icona** dall'elenco di **elementi** , quindi impostare il campo **dimensione** (questa dimensione viene archiviata nel registro di sistema, in **HKEY \_ Current \_ User \\ Control Panel, desktop \\ WindowMetrics \\ Shell Icon Size**).
3.  Fare clic su **Plus** , quindi selezionare la casella di controllo **Usa icone grandi** .

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>Per recuperare la dimensione dell'icona della shell grande

1.  Usare la funzione [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) con **SHGFI \_ SHELLICONSIZE** per recuperare un handle per l'elenco di immagini di sistema.
2.  Chiamare quindi la funzione [**ImageList \_ GetIconSize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) per ottenere le dimensioni dell'icona.

Il menu Start usa le icone Shell Small o Shell large, a seconda che sia selezionata la casella di controllo **Usa icone grandi** .

L'applicazione deve fornire gruppi di immagini icona nelle dimensioni seguenti:

-   48x48, 256 colore
-   32x32, 16 colori
-   16x16 pixel, 16 colori

Quando si compila la struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) da usare per la registrazione della classe della finestra, impostare il membro **HICON** sull'icona 32x32 e il membro **hIconSm** sull'icona 16x16. Per altre informazioni sulle icone delle classi, vedere [Icone di classe](/windows/desktop/winmsg/about-window-classes).

## <a name="icon-creation"></a>Creazione di icone

Le icone standard sono predefinite, quindi non è necessario crearle. Per usare un'icona standard, un'applicazione può ottenere il relativo handle usando la funzione [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Un *handle di icona* è un valore univoco del tipo **HICON** che identifica un'icona standard o personalizzata.

Per creare un'icona personalizzata per un'applicazione, si usa in genere un'applicazione grafica e si include la [risorsa icona](./icon-resource.md) nel file di definizione delle risorse dell'applicazione. In fase di esecuzione, è possibile chiamare [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) per recuperare un handle per l'icona. Una risorsa icona può contenere un gruppo di immagini per diversi dispositivi di visualizzazione. **LoadIcon** e **LoadImage** selezionano automaticamente l'icona più appropriata del gruppo per il dispositivo di visualizzazione corrente.

Un'applicazione può anche creare un'icona personalizzata in fase di esecuzione usando la funzione [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , che crea un'icona basata sul contenuto di una struttura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . La funzione [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) riempie la struttura con le coordinate sensibili e le informazioni sulla bitmap della maschera di bit e sulla bitmap dei colori per l'icona.

Le applicazioni devono implementare icone personalizzate come risorse e usare [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) o [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea), anziché creare l'icona in fase di esecuzione. L'uso delle risorse icona consente di evitare la dipendenza dal dispositivo, semplifica la localizzazione e consente alle applicazioni di condividere forme icona.

La funzione [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) consente a un'applicazione di esplorare le risorse del sistema e creare icone e cursori in base ai dati delle risorse. **CreateIconFromResourceEx** crea un'icona basata sui dati di risorsa binari da altri file eseguibili o dll. Un'applicazione deve precedere questa funzione con le chiamate alla funzione [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) e a diverse funzioni di risorsa. **LookupIconIdFromDirectoryEx** restituisce l'identificatore dei dati dell'icona più appropriati per il dispositivo di visualizzazione corrente.

## <a name="icon-display"></a>Visualizzazione icona

È possibile recuperare l'immagine per un'icona usando la funzione [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) ed è possibile crearla usando la funzione [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Per creare l'immagine predefinita per un'icona, specificare il flag **di \_ compatibilità** con nella chiamata a **DrawIconEx**. Se non si specifica il flag **di \_ compatibilità** con, **DrawIconEx** disegna l'icona usando l'immagine specificata dall'utente.

Quando il sistema Visualizza un'icona, deve estrarre l'immagine dell'icona appropriata dal file con estensione exe o dll. Il sistema usa i passaggi seguenti per selezionare l'immagine dell'icona:

1.  Selezionare la **risorsa \_ \_ icona del gruppo RT** . Se esiste più di una risorsa di questo tipo, il sistema usa la prima risorsa elencata nella bisaccia delle risorse.
2.  Selezionare l'immagine **dell' \_ icona RT** appropriata dalla **risorsa \_ \_ icona del gruppo RT** . Se esiste più di un'immagine, il sistema usa i criteri seguenti per scegliere un'immagine:
    -   -   Viene scelta l'immagine più vicina alle dimensioni richieste.
        -   Se sono presenti due o più immagini di tale dimensione, viene scelto quello che corrisponde alla profondità di colore della visualizzazione.
        -   Se nessuna immagine corrisponde esattamente alla profondità del colore dello schermo, viene scelta l'immagine con la profondità di colore maggiore che non supera la profondità di colore della visualizzazione. Se tutti superano la profondità del colore, viene scelto quello con la profondità del colore più bassa.

> [!Note]  
> Il sistema considera come uguali tutte le profondità di colore di 8 o più BPP. Di conseguenza, non è possibile includere un'immagine a colori 16x16 256 e un'immagine 16x16 a 16 colori nella stessa risorsa. il sistema sceglierà semplicemente il primo rilevato. Quando la visualizzazione è in modalità a 8 BPP, il sistema sceglierà un'icona a 16 colori sull'icona a colori 256 e visualizzerà tutte le icone usando la tavolozza predefinita del sistema.

 

Per visualizzare un'icona animata, usare un controllo statico, come illustrato nel frammento di codice seguente.


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>Icona di distruzione

Quando per un'applicazione non è più necessaria un'icona creata utilizzando la funzione [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , l'icona deve essere eliminata. La funzione [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) Elimina l'handle dell'icona e libera la memoria usata dall'icona. Le applicazioni devono usare questa funzione solo per le icone create con **CreateIconIndirect**; non è necessario eliminare altre icone.

## <a name="icon-duplication"></a>Duplicazione delle icone

La funzione [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) copia un handle di icona. Questo consente a un'applicazione o a una DLL di ottenere un proprio handle per un'icona di proprietà di un altro modulo. Quindi, se l'altro modulo viene liberato, l'applicazione che ha copiato l'icona sarà comunque in grado di usare l'icona.

La funzione [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) crea una nuova icona basata sull'icona di origine specificata. La nuova icona può essere maggiore o minore dell'icona di origine.

Per informazioni sull'aggiunta, la rimozione o la sostituzione di risorse icona nei file eseguibili (con estensione exe), vedere [risorse](resources.md).

La funzione [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) esegue una copia effettiva dell'icona.

 

 