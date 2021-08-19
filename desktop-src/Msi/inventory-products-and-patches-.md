---
description: "Gli utenti e le applicazioni con privilegi amministrativi possono usare le Windows installer per eseguire l'inventario delle applicazioni, delle funzionalità, dei componenti e delle patch del programma di installazione di Windows installate nel sistema. A partire da Windows Installer&160;3.0, gli utenti e le applicazioni con privilegi di amministratore possono enumerare le applicazioni, le funzionalità, i componenti e le patch del programma di installazione di Windows installati nel sistema da tutti gli \\# utenti. Gli amministratori e le applicazioni possono ottenere informazioni su un prodotto o una patch per un determinato utente o per tutti gli utenti del sistema. Le applicazioni possono ottenere lo stato della funzionalità o del componente per un determinato utente. Le funzioni di inventario disponibili a partire da Windows Installer&160;3.0 possono limitare l'ambito degli elementi trovati dal contesto di installazione e dal contesto \\# utente. Esistono tre contesti di installazione possibili: per utente, per computer e gestito per utente. Il contesto utente può essere un utente specifico o tutti gli utenti nel sistema. Le versioni delle funzioni di inventario del programma di installazione di Windows precedenti Windows Installer&160;3.0 possono enumerare solo gli elementi installati nel sistema nel contesto del computer o nel contesto per utente \\# dell'utente corrente. Questa limitazione impedisce un inventario completo di tutti i Windows e le patch del programma di installazione installati nel sistema da utenti diversi dall'utente corrente. Enumerazione di prodottiEnumerazione di patchObtaining Product InformationObtaining Patch InformationObtaining Component State InformationObtaining Feature State Information"
ms.assetid: ef95c3c8-b4c8-4305-8aa2-07ec74b3121b
title: Uso Windows programma di installazione per l'inventario di prodotti e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9406d0984e58efdb8344fbf8974234690e3a6aaeb1cc697b5a76e6af940554e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013229"
---
# <a name="using-windows-installer-to-inventory-products-and-patches"></a>Uso Windows programma di installazione per l'inventario di prodotti e patch

Gli utenti e le applicazioni con privilegi amministrativi possono usare le Windows installer per eseguire l'inventario delle applicazioni, delle funzionalità, dei componenti e delle patch del programma di installazione di Windows installate nel sistema.

A partire da Windows Installer 3.0, gli utenti e le applicazioni con privilegi di amministratore possono enumerare le applicazioni, le funzionalità, i componenti e le patch del programma di installazione di Windows installati nel sistema da tutti gli utenti. Gli amministratori e le applicazioni possono ottenere informazioni su un prodotto o una patch per un determinato utente o per tutti gli utenti del sistema. Le applicazioni possono ottenere lo stato della funzionalità o del componente per un determinato utente.

Le funzioni di inventario disponibili a partire da Windows Installer 3.0 possono limitare l'ambito degli elementi trovati dal contesto di installazione e dal contesto utente. Esistono tre contesti di installazione possibili: per utente, per computer e gestito per utente. Il contesto utente può essere un utente specifico o tutti gli utenti nel sistema.

Le versioni delle funzioni di inventario del programma di installazione di Windows precedenti Windows Installer 3.0 possono enumerare solo gli elementi installati nel sistema nel contesto del computer o nel contesto per utente dell'utente corrente. Questa limitazione impedisce un inventario completo di tutti i Windows e le patch del programma di installazione installati nel sistema da utenti diversi dall'utente corrente.

-   [Enumerazione dei prodotti](#enumerating-products)
-   [Enumerazione delle patch](#enumerating-patches)
-   [Recupero di informazioni sul prodotto](#obtaining-product-information)
-   [Recupero delle informazioni sulla patch](#obtaining-patch-information)
-   [Recupero di informazioni sullo stato dei componenti](#obtaining-component-state-information)
-   [Recupero di informazioni sullo stato delle funzionalità](#obtaining-feature-state-information)

## <a name="enumerating-products"></a>Enumerazione dei prodotti

Usare la [**funzione MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per enumerare Windows di installazione installate nel sistema. Questa funzione può trovare tutte le installazioni per computer e per utente delle applicazioni (gestite e non gestite) per l'utente corrente e altri utenti nel sistema. Usare il *parametro dwContext* per specificare il contesto di installazione da trovare. È possibile specificare uno o qualsiasi combinazione dei contesti di installazione possibili. Usare il *parametro szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="enumerating-patches"></a>Enumerazione delle patch

Usare la [**funzione MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) per trovare le patch applicate a un'applicazione. Questa funzione può trovare le patch applicate per una determinata applicazione o per tutte le applicazioni nel sistema. Questa funzione può trovare le patch applicate a tutte le installazioni per computer e per utente delle applicazioni (gestite e non gestite) per l'utente corrente e altri utenti nel sistema.

È possibile usare il contesto di installazione e il contesto utente per limitare l'enumerazione delle patch a un contesto specifico o in tutti i contesti. Usare il *parametro dwContext* per specificare il contesto di installazione da trovare. È possibile specificare uno o qualsiasi combinazione dei contesti di installazione possibili. Usare il *parametro szUserSid* per specificare il contesto utente delle applicazioni da trovare.

**Per enumerare le patch applicate a tutti i prodotti annunciati o installati da tutti gli utenti del sistema**

-   Chiamare la [**funzione MsiEnumPatchesEx.**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
    -   Usare **NULL** per il valore del *parametro szProductCode.*
    -   Usare "s-1-1-0" per il valore del *parametro szUserSid.*
    -   Usare "MSIINSTALLCONTEXT \_ ALL" per il valore del *parametro dwContext.*

**Per enumerare le patch applicate a tutti i prodotti annunciati o installati da tutti gli utenti del sistema**

1.  Chiamare la [**funzione MsiEnumProductsEx.**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)

    -   Usare **NULL** per il valore del *parametro szProductCode.*
    -   Usare "s-1-1-0" per il valore del *parametro szUserSid.*
    -   Usare "MSIINSTALLCONTEXT \_ ALL" per il valore del *parametro dwContext.*

    La funzione fornisce un codice prodotto, un contesto utente e un contesto di installazione per ogni applicazione trovata.

2.  Per ogni applicazione enumerata nel passaggio 1, chiamare [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa) per enumerare le patch.

    Usare i codici prodotto, i contesti utente e i contesti di installazione ottenuti da [**MsiEnumProductsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa) per i valori *di szProductCode,* *szUserSid* e *dwContext* e ogni chiamata di funzione **MsiEnumProductsEx.**

## <a name="obtaining-product-information"></a>Recupero di informazioni sul prodotto

Usare la [**funzione MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) per ottenere informazioni sulle applicazioni annunciate o installate nel sistema e sulle proprietà che possono essere recuperate. Questa funzione può ottenere informazioni per un'istanza di un'applicazione installata con un account utente diverso dall'utente corrente, ma non può eseguire query su un'istanza di un prodotto annunciato in un contesto non gestito per utente per un account utente diverso dall'utente corrente.

È possibile specificare il contesto di installazione e il contesto utente per limitare le informazioni per le applicazioni installate in un contesto specifico. Usare il *parametro dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Usare il *parametro szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="obtaining-patch-information"></a>Recupero delle informazioni sulla patch

Un'applicazione può chiamare la [**funzione MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) per eseguire una query per ottenere informazioni sull'applicazione di una patch a un'istanza specificata di un prodotto. Proprietà come **LocalPackage,** [**Transforms**](transforms.md)e **State** possono essere recuperate usando questa funzione. Non tutti i valori delle proprietà sono garantiti per le applicazioni non gestite per utente se l'utente non è attualmente connesso al computer. È possibile specificare solo uno dei contesti di installazione possibili.

È possibile specificare il contesto di installazione e il contesto utente per limitare le informazioni alle patch applicate alle applicazioni installate in un contesto specifico. Usare il *parametro dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Usare il *parametro szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="obtaining-component-state-information"></a>Recupero di informazioni sullo stato dei componenti

Le applicazioni possono chiamare la [**funzione MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea) per ottenere lo stato installato per un componente. Questa funzione determina se il componente è installato in locale o installato per l'esecuzione dall'origine. La funzione può eseguire una query per un componente di un'istanza di un'applicazione installata con account utente diversi dall'utente corrente, a condizione che il prodotto non sia annunciato nel contesto non gestito per utente per un account utente diverso dall'utente corrente.

È possibile specificare un contesto di installazione e un contesto utente per ottenere lo stato dei componenti per le applicazioni installate in un contesto specifico. Usare il *parametro dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Usare il *parametro szUserSid* per specificare il contesto utente delle applicazioni da trovare.

## <a name="obtaining-feature-state-information"></a>Recupero di informazioni sullo stato delle funzionalità

Le applicazioni possono chiamare la [**funzione MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa) per ottenere lo stato installato per una funzionalità del prodotto. Questa funzione determina se la funzionalità viene annunciata, installata in locale o installata per l'esecuzione dall'origine. La funzione può essere usata per eseguire query su qualsiasi funzionalità di un'istanza di un'applicazione installata nell'account computer o in qualsiasi contesto nell'account utente corrente o nel contesto gestito per utente in qualsiasi account utente diverso dall'utente corrente. Questa funzione non può eseguire query per un'applicazione installata nel contesto non gestito per utente per un account utente diverso dall'utente corrente. È possibile specificare solo uno dei contesti di installazione possibili.

È possibile specificare un contesto di installazione e un contesto utente per ottenere lo stato delle funzionalità per le applicazioni installate in un contesto specifico. Usare il *parametro dwContext* per specificare il contesto di installazione da trovare. È possibile specificare solo uno dei contesti di installazione possibili. Usare il *parametro szUserSid* per specificare il contesto utente delle applicazioni da trovare.

 

 



