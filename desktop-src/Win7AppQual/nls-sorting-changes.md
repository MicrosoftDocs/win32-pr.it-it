---
description: Modifiche all'ordinamento NLS
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Modifiche all'ordinamento NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088059"
---
# <a name="nls-sorting-changes"></a>Modifiche all'ordinamento NLS

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows XP, Windows Vista, Windows 7  
**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Alta  
**Frequenza** - Bassa (poche app sono influenzate, ma in caso di impatto, sempre interrotte)  


## <a name="description"></a>Descrizione

Le funzioni NLS (National Language Support) consentono alle applicazioni di supportare le diverse esigenze specifiche della lingua e delle impostazioni locali degli utenti in tutto il mondo. Le nuove versioni di Windows includono quasi sempre modifiche NLS. Questa modifica influisce sulle regole di confronto e sull'ordinamento e pertanto sulle applicazioni con indici persistenti.

Una tabella delle regole di confronto include due numeri che ne identificano la versione (revisione): la versione definita e la versione NLS. Entrambe le versioni sono valori DWORD, costituiti da una versione principale e una versione secondaria. Il primo byte di un valore è riservato, i due byte successivi rappresentano la versione principale e l'ultimo byte rappresenta la versione secondaria. In termini esadecimali, il modello è 0xRRMMMMmm, dove R è uguale a Reserved, M è uguale a major e m è uguale a minor. Ad esempio, una versione principale di 3 con una versione secondaria di 4 è rappresentata come 0x304.

Per una versione principale, uno o più punti di codice cambiano in modo che l'applicazione deve indicizzare nuovamente tutti i dati affinché i confronti siano validi. Per una versione secondaria, non viene spostato nulla, ma vengono aggiunti punti di codice. Per questo tipo di versione, l'applicazione deve solo indicizzare nuovamente le stringhe con valori precedentemente non ordinabili. Di seguito è riepilogato il significato dei numeri di versione in relazione alle modifiche dei dati nelle tabelle delle eccezioni specifiche delle impostazioni locali e nelle tabelle predefinite:

**NLSVersion Major:** modifica dei punti di codice nelle tabelle 'exception' o specifiche delle impostazioni locali  
**NLSVersion Minor:** sono stati aggiunti nuovi punti di codice nelle tabelle 'exception' o specifiche delle impostazioni locali  
**DefinedVersion Major:** modifica dei punti di codice nella tabella predefinita  
**DefinedVersion Minor:** sono stati aggiunti nuovi punti di codice nella tabella predefinita  


**Ordinamento dei numeri di versione per le versioni rilasciate:**



| Sistema operativo    | Versione           | Versione (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/D : nessuna API GetNLSVersion() |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestazione

Le applicazioni (ad esempio i database) con indici permanenti che non controllano la versione NLS e ri-indicizzano in caso di modifica della versione non riusciranno a ordinare correttamente o potrebbero non fornire i risultati richiesti.

Nel caso delle interfacce utente, gli elenchi (ad esempio, alfabetico, numerico, alfanumerico, simboli e così via) possono essere ordinati in modo non corretto.

## <a name="solution"></a>Soluzione

L'applicazione può chiamare **GetNLSVersionEx** (Windows Vista o versioni successive) o **GetNLSVersion** (prima di Windows Vista) per recuperare sia la versione definita che la versione NLS per una tabella delle regole di confronto.

-   GetNLSVersionEx:

*Recupera informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate in base al nome*  
Questa funzione consente a un'applicazione come Active Directory di determinare se una modifica NLS influisce sulle impostazioni locali usate per una particolare tabella di indice. In caso contrario, non è necessario indicizzare nuovamente la tabella. Per altre informazioni, vedere Gestione delle informazioni sulle impostazioni locali e sulla lingua.  
Questa funzione supporta impostazioni locali personalizzate. Se *lpLocaleName* specifica impostazioni locali supplementari, i dati recuperati sono i dati corretti per l'ordine delle regole di confronto associato alle impostazioni locali supplementari.  

**Nota:** Le versioni di Windows precedenti a Windows Vista non **supportano GetNLSVersionEx.**  


-   GetNLSVersion (da usare per le applicazioni in esecuzione in versioni di Windows precedenti a Windows Vista):

*Recupera informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate dall'identificatore*  
Questa funzione consente a un'applicazione come Active Directory di determinare se una modifica NLS influisce sull'identificatore delle impostazioni locali usato per una particolare tabella di indice. In caso contrario, non è necessario indicizzare nuovamente la tabella. Per altre informazioni, vedere Gestione delle informazioni sulle impostazioni locali e sulla lingua.  
**Nota:** Questa funzione recupera informazioni solo sulle impostazioni locali specificate dall'identificatore. La **funzione GetNLSVersionEx** supporta impostazioni locali, funzionalità e nomi RFC 4646 aggiuntivi. Tuttavia, le versioni di Windows precedenti a Windows Vista non **supportano GetNLSVersionEx.**  
Le applicazioni destinate a essere eseguite solo in Windows Vista e versioni successive devono **usare GetNLSVersionEx** in preferenza per questa funzione. **GetNLSVersionEx** offre un buon supporto per le impostazioni locali supplementari.  


## <a name="compatibility-test"></a>Test di compatibilità

**Passaggi per determinare se una versione delle regole di confronto è stata modificata, ovvero se è necessario eseguire di nuovo l'indicizzazione:**

-   **Usare GetNLSVersionEx() per** recuperare una **struttura NLSVERSIONINFOEX** durante l'indicizzazione originale dei dati.
-   Archiviare le proprietà seguenti con l'indice per identificare la versione:  **NLSVERSIONINFOEX.dwNLSVersion** e **NLSVERSIONINFOEX.dwDefinedVersion:** queste due proprietà insieme specificano la versione della tabella di ordinamento in uso.  
    **NLSVERSIONINFOEX.dwEffectiveId:** specifica le impostazioni locali valide dell'ordinamento. Le impostazioni locali personalizzate puntano all'ordinamento delle impostazioni locali predefinite.  
    
-   Quando si usa l'indice, **usare GetNlsVersionEx()** per individuare la versione dei dati.
-   Se una delle tre proprietà è stata modificata, i dati di ordinamento in uso potrebbero restituire risultati diversi e qualsiasi indicizzazione potrebbe non riuscire a trovare i record.
-   Se si sa che i dati non contengono punti di codice Unicode non validi, ovvero tutte le stringhe hanno restituito **TRUE** da una chiamata a **IsNLSDefinedString(),** è possibile considerarli uguali se solo il byte basso di **dwNLSVersion** e **dwDefinedVersion** è stato modificato (le versioni secondarie descritte in precedenza).

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Internazionalizzazione per le applicazioni di Windows](../intl/international-support.md)
-   [Funzione GetNLSVersionEx](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [Funzione GetNLSVersion](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Come determinare se la versione delle regole di confronto è stata modificata](/archive/blogs/shawnste/)

 

 
