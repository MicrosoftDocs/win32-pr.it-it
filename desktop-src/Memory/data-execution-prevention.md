---
description: Protezione esecuzione programmi (DEP) è una funzionalità di protezione della memoria a livello di sistema incorporata nel sistema operativo a partire da Windows XP e Windows Server 2003.
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: Protezione esecuzione programmi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311742"
---
# <a name="data-execution-prevention"></a>Protezione esecuzione programmi

Protezione esecuzione programmi (DEP) è una funzionalità di protezione della memoria a livello di sistema incorporata nel sistema operativo a partire da Windows XP e Windows Server 2003. DEP consente al sistema di contrassegnare una o più pagine di memoria come non eseguibili. Contrassegnare le aree di memoria come non eseguibile significa che non è possibile eseguire il codice da tale area di memoria, rendendo più difficile l'exploit dei sovraccarichi del buffer.

DEP impedisce l'esecuzione del codice da pagine di dati quali heap, stack e pool di memoria predefiniti. Se un'applicazione tenta di eseguire il codice da una pagina di dati protetta, si verifica un'eccezione di violazione dell'accesso alla memoria e, se l'eccezione non viene gestita, il processo chiamante viene terminato.

DEP non è progettato per essere una difesa completa contro tutti gli exploit; è concepito come un altro strumento che è possibile usare per proteggere l'applicazione.

## <a name="how-data-execution-prevention-works"></a>Funzionamento della prevenzione dell'esecuzione dei dati

Se un'applicazione tenta di eseguire il codice da una pagina protetta, l'applicazione riceve un'eccezione con la **violazione di \_ accesso \_ allo stato** del codice di stato. Se l'applicazione deve eseguire codice da una pagina di memoria, deve allocare e impostare gli attributi di [protezione della memoria](memory-protection.md) virtuale appropriati. La memoria allocata deve essere contrassegnata come **\_ esecuzione pagina**, esecuzione **\_ \_ lettura pagina**, **pagina \_ esecuzione \_ ReadWrite** o **pagina \_ esecuzione \_ WRITECOPY** durante l'allocazione della memoria. Le allocazioni di heap effettuate chiamando le funzioni **malloc** e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) non sono eseguibili.

Le applicazioni non possono eseguire codice dall'heap di processo predefinito o dallo stack.

DEP viene configurato all'avvio del sistema in base all'impostazione dei criteri di protezione della pagina No-Execute nei dati di configurazione di avvio. Un'applicazione può ottenere l'impostazione dei criteri corrente chiamando la funzione [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) . A seconda dell'impostazione dei criteri, un'applicazione può modificare l'impostazione DEP per il processo corrente chiamando la funzione [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) .

## <a name="programming-considerations"></a>Considerazioni sulla programmazione

Un'applicazione può utilizzare la funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) per allocare memoria eseguibile con le opzioni di protezione della memoria appropriate. È consigliabile che un'applicazione configurata come minimo l'opzione di protezione della memoria di **\_ esecuzione della pagina** . Dopo la generazione del codice eseguibile, è consigliabile che l'applicazione imposti Protezioni di memoria per impedire l'accesso in scrittura alla memoria allocata. Le applicazioni possono impedire l'accesso in scrittura alla memoria allocata tramite la funzione [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) . Non consentire l'accesso in scrittura garantisce la massima protezione per le aree eseguibili dello spazio degli indirizzi del processo. È consigliabile tentare di creare applicazioni che utilizzano lo spazio degli indirizzi eseguibile più piccolo possibile, riducendo al minimo la quantità di memoria esposta allo sfruttamento della memoria.

È anche necessario provare a controllare il layout della memoria virtuale dell'applicazione e creare aree eseguibili. Queste aree eseguibili devono trovarsi in uno spazio di memoria inferiore rispetto alle aree non eseguibili. Individuando le aree eseguibili sotto le aree non eseguibili, è possibile evitare l'overflow del buffer nell'area eseguibile della memoria.

## <a name="application-compatibility"></a>Compatibilità delle applicazioni

Alcune funzionalità dell'applicazione non sono compatibili con DEP. Le applicazioni che eseguono la generazione di codice dinamico (ad esempio la generazione di codice JIT) e non contrassegnano in modo esplicito il codice generato con l'autorizzazione Execute possono presentare problemi di compatibilità nei computer che utilizzano DEP. Le applicazioni scritte nella Active Template Library (ATL) versione 7,1 e versioni precedenti possono tentare di eseguire codice sulle pagine contrassegnate come non eseguibili, che attiva un errore NX e termina l'applicazione. Per ulteriori informazioni, vedere [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy). Per il corretto funzionamento, è necessario aggiornare la maggior parte delle applicazioni che eseguono azioni incompatibili con DEP.

Un numero ridotto di file eseguibili e librerie può contenere codice eseguibile nella sezione dati di un file di immagine. In alcuni casi, le applicazioni possono inserire piccoli segmenti di codice, comunemente definiti thunk, nelle sezioni di dati. Tuttavia, DEP contrassegna le sezioni del file di immagine che viene caricato in memoria come non eseguibile, a meno che alla sezione non sia applicato l'attributo Executable.

Pertanto, è necessario eseguire la migrazione del codice eseguibile nelle sezioni di dati a una sezione di codice oppure la sezione di dati che contiene il codice eseguibile deve essere contrassegnata in modo esplicito come eseguibile. L'attributo eseguibile **Image \_ SCN \_ mem \_ Execute** deve essere aggiunto al campo **caratteristiche** dell'intestazione della sezione corrispondente per le sezioni che contengono codice eseguibile. Per ulteriori informazioni sull'aggiunta di attributi a una sezione, vedere la documentazione inclusa nel linker.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione esecuzione programmi (TechNet)](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[Come configurare la protezione della memoria](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[Articolo della Knowledge 875352](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
