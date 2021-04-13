---
title: Risoluzione dei conflitti di nome di funzione/proprietà nell'automazione nelle estensioni
description: In questo argomento, \ 0034; oggetto \ 0034; indica l'oggetto, nel suo complesso, in cui un client ADSI lo Visualizza. Ovvero ADSI e tutte le relative estensioni.
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- Risoluzione dei conflitti di nomi di proprietà e funzioni nell'automazione nelle estensioni
- estensioni ADSI, risoluzione dei conflitti di funzioni e nomi di proprietà in automazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a7ac99b99ecdf0ee1b940f066d9e8166a15542
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399717"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>Risoluzione dei conflitti di nome di funzione/proprietà nell'automazione nelle estensioni

In questo argomento, "Object" indica l'oggetto, come un intero, come un client ADSI che lo Visualizza. Ovvero ADSI e tutte le relative estensioni.

## <a name="same-function-name-with-the-same-parameters"></a>Stesso nome di funzione con gli stessi parametri

Se due o più interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) doppie in un oggetto supportano una proprietà o un metodo con lo stesso nome, ad esempio **func1**, la chiamata viene determinata in base ai criteri seguenti. Se il client dispone di un puntatore a una delle interfacce duali che supportano un metodo denominato **func1** e se l'ambiente di automazione supporta l'accesso vtable, **func1** viene richiamato direttamente tramite l'accesso a vtable di ADSI.

Se una delle condizioni precedenti è false, [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) vengono chiamati per richiamare **func1**.

Per ulteriori informazioni e una breve spiegazione su come un client può aggiungere un puntatore a una doppia interfaccia e una descrizione dei tipi di ambienti che supportano l'accesso a vtable, vedere [associazione tardiva rispetto all'accesso a vtable nel modello di estensione ADSI](late-binding-vs--vtable-access-in-the-adsi-extension-model.md).

Poiché tutti gli oggetti di estensione reindirizzano le funzioni [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a aggregator, l'aggregator controlla quale **func1** viene richiamato. Le regole sono:

-   Se una qualsiasi interfaccia, e ne sarà presente solo una, se presente, in Aggregator (ADSI) supporta una funzione denominata **func1**, l'aggregator richiama il proprio **func1**.
-   In caso contrario, l'aggregatore passa attraverso ognuna delle relative estensioni, nell'ordine elencato nel registro di sistema, e trova la prima estensione che implementa una funzione denominata **func1**. È possibile, ma improbabile, che più interfacce dual [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) in questa prima estensione abbiano una funzione denominata **func1**. L'estensione deve determinare quali **func1** devono sempre essere richiamati in automazione.

## <a name="same-function-name-with-different-parameters"></a>Stesso nome di funzione con parametri diversi

Nella sezione precedente è stato illustrato come risolvere i conflitti di nomi di funzione, ovvero i nomi di funzione che hanno lo stesso nome di funzione e lo stesso elenco di parametri, ad esempio numero, tipo e ordine, quando si verifica in automazione. Cosa accade se due funzioni hanno lo stesso nome ma parametri diversi? Se un client ADSI richiama la funzione utilizzando [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) senza utilizzare più nomi per specificare i parametri, il modello di estensione ADSI non può distinguere le funzioni. In base allo schema di risoluzione descritto in precedenza, la prima estensione nel registro di sistema che supporta questa funzione tramite una delle sue interfacce ha la versione di questa funzione richiamata e la chiamata potrebbe non riuscire o restituire risultati non corretti.

Ad esempio:

-   Extn1 (prima nel registro di sistema in classe CA-priorità superiore) supporta **IInterface1**.
-   Extn2 (terzo nel registro di sistema in classe CA-priorità inferiore) supporta **IInterface2**.
-   **IInterface1** supporta **Method1 (int param1, int param2)**.
-   **IInterface2** supporta **Method1 (int param1)**.

Un client ADSI dispone di un puntatore a interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) a un oggetto della classe CA. Desidera richiamare **IInterface2:: Method1**. Se il client chiama "pDispatch->GetIDsOfNames (IID \_ null, rgszNames, 1, My \_ LCID, rgDispId)" semplicemente archiviando il nome della funzione "Method1" *in \[ rgszNames \] 0*, viene richiamato **IInterface1:: Method1** anziché l'oggetto **IInterface2:: Method1** desiderato e la funzione ha esito negativo perché il numero di parametri è diverso.

Per ridurre al minimo questo problema, gli sviluppatori di estensioni possono anteporre i nomi di funzione ai relativi identificatori specifici ed evitare progettazioni di interfacce che usano funzioni con lo stesso nome, ma parametri diversi.

Se si verifica un conflitto di nomi, i client ADSI possono evitare il problema tramite l'accesso diretto a vtable se l'interfaccia è una doppia interfaccia. Se non è possibile accedere direttamente a vtable, i client ADSI devono chiamare [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con più nomi, specificando i nomi di funzione e i parametri nella matrice *rgszNames* descritta in precedenza.

Visual Basic 5 non chiama la funzione [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) con più nomi. Ovvero passa solo il nome della funzione a **GetIDsOfNames**, ma non gli argomenti. Tuttavia, Visual Basic 5 consente agli utenti di richiamare una funzione tramite accesso diretto a vtable, anziché richiamare la funzione **IDispatch:: GetIDsOfNames** se l'interfaccia è un'interfaccia duale. Gli sviluppatori devono usare l'accesso diretto a vtable, se possibile.

Per ulteriori informazioni sulla risoluzione dei conflitti di nome, vedere l' [esempio per la risoluzione dei conflitti di nomi di funzione](example-for-resolving-function-name-conflicts.md).

 

 