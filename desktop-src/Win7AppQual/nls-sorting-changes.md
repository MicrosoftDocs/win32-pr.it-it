---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: Modifiche di ordinamento NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4935a6874e28270e73904eb352cd6332e650b7
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314954"
---
# <a name="nls-sorting-changes"></a>Modifiche di ordinamento NLS

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** -Windows XP, Windows Vista, Windows 7  
**Server** : windows Server 2003, windows Server 2008, windows Server 2008 R2  










## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -alta  
**Frequenza** -bassa (poche app interessate, ma se interessate, sempre interrotte)  


## <a name="description"></a>Descrizione

Le funzioni NLS (National Language Support) aiutano le applicazioni a supportare le diverse esigenze specifiche per la lingua e le impostazioni locali degli utenti in tutto il mondo. Le nuove versioni di Windows includono quasi sempre le modifiche NLS. Questa modifica influiscono sulle regole di confronto e l'ordinamento, quindi sulle applicazioni con indici permanenti.

Una tabella delle regole di confronto contiene due numeri che ne identificano la versione (revisione), ovvero la versione definita e la versione NLS. Entrambe le versioni sono valori DWORD, composti da una versione principale e una versione secondaria. Il primo byte di un valore è riservato, i due byte successivi rappresentano la versione principale e l'ultimo byte rappresenta la versione secondaria. In termini esadecimali, il modello è 0xRRMMMMmm, dove R è uguale a reserved, M è uguale a Major e m è uguale a minor. Ad esempio, una versione principale di 3 con una versione secondaria di 4 viene rappresentata come 0x304.

Per una versione principale, uno o più punti di codice cambiano in modo che l'applicazione debba reindicizzare tutti i dati affinché i confronti siano validi. Per una versione secondaria, nulla viene spostato, ma vengono aggiunti punti di codice. Per questo tipo di versione, l'applicazione deve solo reindicizzare le stringhe con valori precedentemente non ordinabili. In sintesi, di seguito sono riportati i numeri di versione in relazione alle modifiche dei dati nelle tabelle delle eccezioni specifiche delle impostazioni locali e nelle tabelle predefinite:

**NLSVersion Major** : punti di codice modificati nelle tabelle ' Exception ' o specifiche delle impostazioni locali  
**NLSVersion minor** -aggiunta di nuovi punti di codice nelle tabelle ' Exception ' o specifiche delle impostazioni locali  
**DefinedVersion Major** : punti di codice modificati nella tabella predefinita  
**DefinedVersion minor** -aggiunta di nuovi punti di codice nella tabella predefinita  


**Ordinamento dei numeri di versione per le versioni rilasciate:**



| Sistema operativo    | Versione           | Versione (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/A-nessuna API GetNLSVersion () |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestazione

Le applicazioni, ad esempio i database, con indici permanenti che non controllano la versione NLS e reindicizzano in caso di modifica della versione non verranno ordinate correttamente o potrebbero non riuscire a fornire i risultati richiesti.

Nel caso di interfacce utente, gli elenchi (ad esempio, alfabetico, numerico, alfanumerico, simboli e così via) potrebbero essere ordinati in modo errato.

## <a name="solution"></a>Soluzione

L'applicazione può chiamare **GetNLSVersionEx** (Windows Vista o versione successiva) o **GetNLSVersion** (prima di Windows Vista) per recuperare sia la versione definita che la versione NLS per una tabella delle regole di confronto.

-   GetNLSVersionEx:

*Recupera le informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate dal nome*  
Questa funzione consente a un'applicazione, ad esempio Active Directory di determinare se una modifica NLS influisca sulle impostazioni locali utilizzate per una determinata tabella dell'indice. In caso contrario, non è necessario reindicizzare la tabella. Per ulteriori informazioni, vedere Gestione delle impostazioni locali e delle informazioni sulla lingua.  
Questa funzione supporta impostazioni locali personalizzate. Se *lpLocaleName* specifica un'impostazione locale supplementare, i dati recuperati sono i dati corretti per l'ordine delle regole di confronto associato alle impostazioni locali supplementari.  

**Nota:** Le versioni di Windows precedenti a Windows Vista non supportano **GetNLSVersionEx**.  


-   GetNLSVersion (utilizzare per le applicazioni in esecuzione nelle versioni di Windows precedenti a Windows Vista):

*Recupera le informazioni sulla versione corrente di una funzionalità NLS specificata per le impostazioni locali specificate dall'identificatore*  
Questa funzione consente a un'applicazione, ad esempio Active Directory di determinare se una modifica NLS influisca sull'identificatore delle impostazioni locali utilizzato per una determinata tabella dell'indice. In caso contrario, non è necessario reindicizzare la tabella. Per ulteriori informazioni, vedere Gestione delle impostazioni locali e delle informazioni sulla lingua.  
**Nota:** Questa funzione recupera informazioni solo sulle impostazioni locali specificate dall'identificatore. La funzione **GetNLSVersionEx** supporta impostazioni locali, funzionalità e nomi RFC 4646 aggiuntivi. Tuttavia, le versioni di Windows precedenti a Windows Vista non supportano **GetNLSVersionEx**.  
Le applicazioni destinate a essere eseguite solo in Windows Vista e versioni successive devono utilizzare **GetNLSVersionEx** in preferenza a questa funzione. **GetNLSVersionEx** offre un supporto efficace per le impostazioni locali aggiuntive.  


## <a name="compatibility-test"></a>Test di compatibilità

**Viene descritta la procedura per stabilire se una versione delle regole di confronto è cambiata (ovvero è necessario reindicizzare):**

-   **Utilizzare GetNLSVersionEx ()** per recuperare una struttura **NLSVERSIONINFOEX** quando si esegue l'indicizzazione originale dei dati.
-   Archiviare le proprietà seguenti con l'indice per identificare la versione:  **NLSVERSIONINFOEX. dwNLSVersion** e **NLSVERSIONINFOEX. dwDefinedVersion** : queste due proprietà insieme specificano la versione della tabella di ordinamento in uso.  
    **NLSVERSIONINFOEX. dwEffectiveId** : specifica le impostazioni locali effettive dell'ordinamento. Le impostazioni locali personalizzate punteranno a un ordinamento delle impostazioni locali nella casella.  
    
-   Quando si utilizza l'indice, utilizzare **GetNlsVersionEx ()** per individuare la versione dei dati.
-   Se una delle tre proprietà è stata modificata, i dati di ordinamento utilizzati potrebbero restituire risultati diversi e qualsiasi indicizzazione potrebbe non riuscire a trovare i record.
-   Se si è certi che i dati non contengono punti di codice Unicode non validi (ovvero, tutte le stringhe restituiscono **true** da una chiamata a **IsNLSDefinedString ()**), è possibile considerare le stesse se solo il byte minimo di **dwNLSVersion** e **dwDefinedVersion** è cambiato (le versioni secondarie descritte in precedenza).

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Internazionalizzazione per le applicazioni di Windows](../intl/international-support.md)
-   [GetNLSVersionEx (funzione)](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion (funzione)](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Come stabilire se la versione delle regole di confronto è stata modificata](/archive/blogs/shawnste/)

 

 
