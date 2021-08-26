---
description: L'applicazione globalizzata deve definire un'ampia gamma di elementi dell'interfaccia utente, ad esempio menu, finestre di dialogo, stringhe della Guida e altri elementi, rappresentati come risorse localizzate.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: Gestione delle risorse MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0b489d10ae28ca0fe7c659153b58c6ee7713e4eda4e1da9d96ffe16ae1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041271"
---
# <a name="mui-resource-management"></a>Gestione delle risorse MUI

L'applicazione globalizzata deve definire un'ampia gamma di elementi dell'interfaccia utente, ad esempio menu, finestre di dialogo, stringhe della Guida e altri elementi, rappresentati come risorse localizzate. La lingua dell'interfaccia utente diventa una delle impostazioni per l'applicazione. Questa sezione descrive la tecnologia delle risorse MUI, che è consigliabile usare per creare le risorse dell'applicazione.

## <a name="features-of-the-mui-resource-technology"></a>Funzionalità della tecnologia delle risorse MUI

La tecnologia delle risorse MUI, esposta in Windows Vista e versioni successive, presenta le caratteristiche seguenti:

-   I file di risorse specifici della lingua vengono archiviati separatamente dal file binario del codice dell'applicazione, in modo che una modifica del codice non influisca sulle risorse.
-   Le risorse per più lingue possono essere distribuite in una singola installazione o in installazioni separate per ogni lingua.
-   Una risorsa viene caricata e visualizzata in base alla lingua dell'applicazione impostata dall'utente.

Questa tecnologia associa le risorse definite in file specifici della lingua a una particolare versione di un file indipendente dalla lingua (LN). Il file LN è un file PE Win32 che rappresenta le risorse binarie del codice dell'applicazione e indipendenti dalla lingua. L'associazione dei file usa un checksum rispecchiato nei dati di configurazione delle risorse contenuti in tutti i file associati. Il caricatore di risorse usa il checksum per verificare che i file contengono la stessa versione delle risorse necessarie. Convalida anche la lingua nel file specifico della lingua con il nome della cartella. Il caricatore non carica un file di risorse se non viene stabilita l'associazione appropriata.

In particolare, il checksum principale viene calcolato dai numeri di versione principale e secondario di un file e dal nome del file (con distinzione tra maiuscole e minuscole), ottenuti dalla risorsa della versione. Questo checksum non deve cambiare tra le versioni RTM e Service Pack dello stesso componente. Inoltre, un checksum del servizio viene usato per determinare la versione appropriata del file di risorse specifico della lingua da caricare. Questo checksum viene calcolato in base alle risorse localizzabili nel file.

MUI fornisce due utilità di risorse che è possibile usare per preparare i file di risorse per l'applicazione. Un'utilità specifica di MUI, denominata MUIRCT, consente di compilare un file LN e i file di risorse specifici della lingua associati. In Windows Vista e versioni successive, anche il compilatore Windows RC è stato modificato per compilare questi file in base alla tecnologia delle risorse MUI. Per la sintassi e i dettagli di questi strumenti, vedere [Utilità per le risorse.](resource-utilities.md)

## <a name="ln-file"></a>LN File

Il file LN per un'applicazione MUI contiene codice eseguibile e risorse indipendenti dalla lingua condivise e installate da tutte le versioni linguistiche dell'applicazione.

## <a name="language-specific-resource-file"></a>Language-Specific file di risorse

Un file di risorse specifico della lingua contiene in genere stringhe dell'interfaccia utente e altri elementi che richiedono la localizzazione per una determinata lingua. L'applicazione MUI usa un file di risorse specifico della lingua per ogni lingua supportata. Il file LN per l'applicazione è lo stesso per ogni file di risorse specifico della lingua.

Se compilati usando la tecnologia delle risorse MUI, i file specifici della lingua hanno un'estensione "mui" e vengono gestiti come segue:

-   I file specifici della lingua associati a un determinato file LN condividono tutti lo stesso nome file, formato aggiungendo l'estensione "mui" al nome file completo (con estensione ) del file LN corrispondente. Ad esempio, un file LN denominato "Myfile.dll" contiene file specifici della lingua denominati "Myfile.dll.mui".
-   I file specifici della lingua si trovano nelle sottocartelle della cartella contenente il file LN. Ogni nome di cartella riflette la lingua.

## <a name="resource-configuration-data"></a>Dati di configurazione delle risorse

Per associare un file LN ai relativi file specifici della lingua, la tecnologia delle risorse MUI usa i dati di configurazione delle risorse, incluso il checksum. La procedura di compilazione della risorsa inserisce queste informazioni in una sezione RC Config di ogni LN e file specifico della lingua. Una forma leggibile di queste informazioni è disponibile tramite l'utilità MUIRCT. Per altre informazioni, vedere [Utilità risorse.](resource-utilities.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni interfaccia utente multilingue](about-multilingual-user-interface.md)
</dt> <dt>

[Utilità per le risorse](resource-utilities.md)
</dt> </dl>

 

 



