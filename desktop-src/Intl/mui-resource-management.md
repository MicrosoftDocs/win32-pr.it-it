---
description: L'applicazione globalizzata deve definire un'ampia gamma di elementi dell'interfaccia utente, ad esempio menu, finestre di dialogo, stringhe della guida e altri elementi, rappresentati come risorse localizzate.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: Gestione delle risorse MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308692"
---
# <a name="mui-resource-management"></a>Gestione delle risorse MUI

L'applicazione globalizzata deve definire un'ampia gamma di elementi dell'interfaccia utente, ad esempio menu, finestre di dialogo, stringhe della guida e altri elementi, rappresentati come risorse localizzate. La lingua dell'interfaccia utente diventa una delle impostazioni dell'applicazione. Questa sezione descrive la tecnologia delle risorse MUI, che è consigliabile usare per creare le risorse dell'applicazione.

## <a name="features-of-the-mui-resource-technology"></a>Funzionalità della tecnologia delle risorse MUI

La tecnologia delle risorse MUI, esposta in Windows Vista e versioni successive, presenta le caratteristiche seguenti:

-   I file di risorse specifici della lingua vengono archiviati separatamente dal file binario del codice dell'applicazione, in modo che una modifica del codice non influisca sulle risorse.
-   Le risorse per più lingue possono essere distribuite in una singola installazione o in installazioni separate per ciascuna lingua.
-   Una risorsa viene caricata e visualizzata in base alla lingua dell'applicazione impostata dall'utente.

Questa tecnologia associa le risorse definite in file specifici della lingua con una particolare versione di un file indipendente dalla lingua (LN). Il file LN è un file PE Win32 che rappresenta il codice dell'applicazione e le risorse indipendenti dalla lingua. L'associazione dei file usa un checksum riflesso nei dati di configurazione delle risorse contenuti in tutti i file associati. Il caricatore di risorse usa il checksum per verificare che i file contengano la stessa versione delle risorse necessarie. Viene inoltre convalidata la lingua nel file specifico della lingua con il nome della cartella. Il caricatore non carica un file di risorse se non è stata stabilita un'associazione appropriata.

In particolare, il checksum principale viene calcolato dai numeri di versione principale e secondaria di un file e dal nome del file (con distinzione tra maiuscole e minuscole), ottenuti dalla risorsa della versione. Questo checksum non deve variare tra le versioni RTM e Service Pack dello stesso componente. Viene inoltre utilizzato un checksum del servizio per determinare la versione appropriata del file di risorse specifico del linguaggio da caricare. Questo checksum viene calcolato in base alle risorse localizzabili del file.

MUI fornisce due utilità di risorse che è possibile usare per preparare i file di risorse per l'applicazione. Un'utilità specifica di MUI, denominata MUIRCT, consente di compilare un file LN e i file di risorse specifici della lingua associati. In Windows Vista e versioni successive, il compilatore Windows RC è stato modificato anche per creare questi file in base alla tecnologia delle risorse MUI. Per la sintassi e i dettagli di questi strumenti, vedere [Utilità risorse](resource-utilities.md).

## <a name="ln-file"></a>LN file

Il file in per un'applicazione MUI contiene codice eseguibile e risorse indipendenti dalla lingua condivise e installate da tutte le versioni in lingua dell'applicazione.

## <a name="language-specific-resource-file"></a>File di risorse Language-Specific

Un file di risorse specifico della lingua contiene in genere le stringhe dell'interfaccia utente e altri elementi che richiedono la localizzazione per una lingua specifica. L'applicazione MUI usa un file di risorse specifico della lingua per ogni lingua supportata. Il file LN per l'applicazione è lo stesso per ogni file di risorse specifico della lingua.

Quando vengono compilate usando la tecnologia delle risorse MUI, i file specifici della lingua hanno un'estensione ". mui" e vengono gestiti come indicato di seguito:

-   I file specifici della lingua associati a un determinato file in condividono lo stesso nome di file, formato dall'aggiunta dell'estensione ". mui" al nome file completo (con estensione) del file nel corrispondente. Ad esempio, in un file denominato "Myfile.dll" sono presenti file specifici della lingua denominati "Myfile.dll. mui".
-   I file specifici della lingua si trovano in sottocartelle della cartella che contiene il file LN. Il nome di ogni cartella riflette il linguaggio.

## <a name="resource-configuration-data"></a>Dati di configurazione delle risorse

Per associare un file LN ai file specifici della lingua, la tecnologia delle risorse MUI usa i dati di configurazione delle risorse, incluso il checksum. La procedura di compilazione delle risorse inserisce queste informazioni in una sezione di configurazione RC di ogni LN e file specifico della lingua. Una forma leggibile di queste informazioni è disponibile tramite l'utilità MUIRCT. Per altre informazioni, vedere [Utilità risorse](resource-utilities.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'interfaccia utente multilingue](about-multilingual-user-interface.md)
</dt> <dt>

[Utilità per le risorse](resource-utilities.md)
</dt> </dl>

 

 



