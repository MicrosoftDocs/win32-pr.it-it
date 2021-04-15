---
description: "Gli utenti e le applicazioni con privilegi amministrativi possono usare funzioni di Windows Installer per eseguire l'inventario di Windows Installer applicazioni, funzionalità, componenti e patch installate nel sistema. A partire da Windows Installer&\\# 160; 3.0, gli utenti e le applicazioni che dispongono di privilegi di amministratore possono enumerare le applicazioni, le funzionalità, i componenti e le patch di Windows Installer installate nel sistema da tutti gli utenti. Gli amministratori e le applicazioni possono ottenere informazioni su un prodotto o una patch per un utente specifico o per tutti gli utenti del sistema. Le applicazioni possono ottenere lo stato della funzionalità o il componente per un utente specifico. Le funzioni di inventario disponibili che iniziano con Windows Installer&\\# 160; 3.0 possono limitare l'ambito degli elementi che devono essere individuati dal contesto di installazione e dall'utente. Esistono tre possibili contesti di installazione: per utente, per computer e gestiti per utente. Il contesto utente può essere un utente specifico o tutti gli utenti del sistema. Le versioni delle funzioni di inventario Windows Installer precedenti al Windows Installer&\\# 160; 3.0 possono solo enumerare gli elementi installati nel sistema nel contesto del computer o nel contesto per utente dell'utente corrente. Questa limitazione impedisce l'inventario completo di tutti i prodotti Windows Installer e le patch installate nel sistema da utenti diversi dall'utente corrente. Enumerazione delle informazioni sullo stato della funzionalità ProductsEnumerating PatchesObtaining Product InformationObtaining patch InformationObtaining"
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: Utilizzo di Windows Installer per l'inventario di prodotti e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7915a8a58954c2e07a3dae9536ed7bae399e416b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525164"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>Utilizzo di Windows Installer per l'inventario di prodotti e patch

Gli utenti e le applicazioni con privilegi amministrativi possono usare funzioni di Windows Installer per eseguire l'inventario di Windows Installer applicazioni, funzionalità, componenti e patch installate nel sistema.

A partire da Windows Installer 3,0, gli utenti e le applicazioni che dispongono di privilegi di amministratore possono enumerare le applicazioni, le funzionalità, i componenti e le patch di Windows Installer installate nel sistema da tutti gli utenti. Gli amministratori e le applicazioni possono ottenere informazioni su un prodotto o una patch per un utente specifico o per tutti gli utenti del sistema. Le applicazioni possono ottenere lo stato della funzionalità o il componente per un utente specifico.

Le funzioni di inventario disponibili a partire da Windows Installer 3,0 possono limitare l'ambito degli elementi che devono essere individuati dal contesto di installazione e dal contesto utente. Esistono tre possibili contesti di installazione: per utente, per computer e gestiti per utente. Il contesto utente può essere un utente specifico o tutti gli utenti del sistema.

Le versioni delle funzioni di inventario Windows Installer precedenti a Windows Installer 3,0 possono solo enumerare gli elementi installati nel sistema nel contesto del computer o nel contesto per utente dell'utente corrente. Questa limitazione impedisce l'inventario completo di tutti i prodotti Windows Installer e le patch installate nel sistema da utenti diversi dall'utente corrente.

-   [Enumerazione dei prodotti](#enumerating-products)
-   [Enumerazione delle patch](#enumerating-patches)
-   [Recupero delle informazioni sul prodotto](#obtaining-product-information)
-   [Recupero delle informazioni sulla patch](#obtaining-patch-information)
-   [Recupero delle informazioni sullo stato del componente](#obtaining-component-state-information)
-   [Recupero delle informazioni sullo stato della funzionalità](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Enumerazione dei prodotti

Utilizzare la funzione [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per enumerare Windows Installer applicazioni installate nel sistema. Questa funzione consente di trovare tutte le installazioni per computer e le installazioni per utente di applicazioni (gestite e non gestite) per l'utente corrente e per gli altri utenti del sistema. Usare il parametro *dwContext* per specificare il contesto di installazione da trovare. È possibile specificare una qualsiasi combinazione dei contesti di installazione possibili. Utilizzare il parametro *szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="enumerating-patches"></a>Enumerazione delle patch

Usare la funzione [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) per trovare le patch applicate per un'applicazione. Questa funzione può individuare le patch applicate per una particolare applicazione o per tutte le applicazioni nel sistema. Questa funzione è in grado di individuare le patch applicate a tutte le installazioni per computer e installazioni per utente (gestite e non gestite) per l'utente corrente e per gli altri utenti del sistema.

È possibile usare il contesto di installazione e il contesto utente per limitare l'enumerazione patch a un particolare contesto o a tutti i contesti. Usare il parametro *dwContext* per specificare il contesto di installazione da trovare. È possibile specificare una qualsiasi combinazione dei contesti di installazione possibili. Utilizzare il parametro *szUserSid* per specificare il contesto utente delle applicazioni da trovare.

**Per enumerare le patch applicate a tutti i prodotti pubblicizzati o installati da tutti gli utenti nel sistema**

-   Chiamare la funzione [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) .
    -   Utilizzare **null** per il valore del parametro *szProductCode* .
    -   Usare "s-1-1-0" per il valore del parametro *szUserSid* .
    -   Usare "MSIINSTALLCONTEXT \_ All" per il valore del parametro *dwContext* .

**Per enumerare le patch applicate a tutti i prodotti pubblicizzati o installati da tutti gli utenti nel sistema**

1.  Chiamare la funzione [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) .

    -   Utilizzare **null** per il valore del parametro *szProductCode* .
    -   Usare "s-1-1-0" per il valore del parametro *szUserSid* .
    -   Usare "MSIINSTALLCONTEXT \_ All" per il valore del parametro *dwContext* .

    La funzione fornisce un codice prodotto, un contesto utente e un contesto di installazione per ogni applicazione individuata.

2.  Per ogni applicazione enumerata nel passaggio 1, chiamare [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) per enumerare le patch.

    Usare i codici prodotto, i contesti utente e i contesti di installazione ottenuti da [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per i valori di *szProductCode*, *szUserSid* e *dwContext* e ogni chiamata di funzione **MsiEnumProductsEx** .

## <a name="obtaining-product-information"></a>Recupero delle informazioni sul prodotto

Utilizzare la funzione [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) per ottenere informazioni sulle applicazioni annunciate o installate nel sistema e sulle proprietà che è possibile recuperare. Questa funzione può ottenere informazioni per un'istanza di un'applicazione installata con un account utente diverso dall'utente corrente, ma non può eseguire una query su un'istanza di un prodotto annunciata in un contesto non gestito per utente per un account utente diverso dall'utente corrente.

È possibile specificare il contesto di installazione e il contesto utente per limitare le informazioni per le applicazioni installate in un particolare contesto. Usare il parametro *dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Utilizzare il parametro *szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="obtaining-patch-information"></a>Recupero delle informazioni sulla patch

Un'applicazione può chiamare la funzione [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) per eseguire una query per ottenere informazioni sull'applicazione di una patch a un'istanza specificata di un prodotto. Con questa funzione è possibile recuperare proprietà quali **LocalPackage**, [**transforms**](transforms.md)e **state** . Non tutti i valori delle proprietà sono sicuramente disponibili per le applicazioni non gestite per utente se l'utente non è attualmente connesso al computer. È possibile specificare solo uno dei contesti di installazione possibili.

È possibile specificare il contesto di installazione e il contesto utente per limitare le informazioni alle patch applicate alle applicazioni installate in un particolare contesto. Usare il parametro *dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Utilizzare il parametro *szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="obtaining-component-state-information"></a>Recupero delle informazioni sullo stato del componente

Le applicazioni possono chiamare la funzione [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) per ottenere lo stato installato per un componente. Questa funzione determina se il componente è installato localmente o installato per l'esecuzione dall'origine. La funzione può eseguire una query per un componente di un'istanza di un'applicazione installata in account utente diversi dall'utente corrente, purché il prodotto non venga annunciato nel contesto non gestito per utente per un account utente diverso dall'utente corrente.

È possibile specificare un contesto di installazione e un contesto utente per ottenere lo stato dei componenti per le applicazioni installate in un particolare contesto. Usare il parametro *dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Utilizzare il parametro *szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="obtaining-feature-state-information"></a>Recupero delle informazioni sullo stato della funzionalità

Le applicazioni possono chiamare la funzione [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) per ottenere lo stato installato per una funzionalità del prodotto. Questa funzione determina se la funzionalità è annunciata, installata localmente o installata per l'esecuzione dall'origine. La funzione può essere utilizzata per eseguire una query su qualsiasi funzionalità di un'istanza di un'applicazione installata nell'account del computer o in qualsiasi contesto con l'account utente corrente o il contesto gestito per utente con qualsiasi account utente diverso dall'utente corrente. Questa funzione non può eseguire una query per un'applicazione installata nel contesto non gestito per utente per un account utente diverso dall'utente corrente. È possibile specificare solo uno dei contesti di installazione possibili.

È possibile specificare un contesto di installazione e un contesto utente per ottenere lo stato delle funzionalità per le applicazioni installate in un particolare contesto. Usare il parametro *dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Utilizzare il parametro *szUserSid* per specificare il contesto utente delle applicazioni da trovare.

 

 



