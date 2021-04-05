---
description: Descrive i reparse point.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Punti di analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ad17af8993da500154dd88690420a563886f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884125"
---
# <a name="reparse-points"></a>Punti di analisi

Un file o una directory può contenere un *reparse point*, ovvero una raccolta di dati definiti dall'utente. Il formato di questi dati viene riconosciuto dall'applicazione che archivia i dati e da un filtro file system, che viene installato per interpretare i dati ed elaborare il file. Quando un'applicazione imposta un reparse point, archivia questi dati, oltre a un *tag reparse*, che identifica in modo univoco i dati archiviati. Quando il file system apre un file con un reparse point, tenta di trovare il filtro file system associato al formato dati identificato dal tag reparse. Se viene trovato un filtro file system, il filtro elabora il file come indicato dai dati di analisi. Se non viene trovato un filtro di file system, l'operazione di apertura file non riesce.

I reparse point, ad esempio, vengono usati per implementare i collegamenti file system NTFS e il server di archiviazione remota Microsoft (RSS). RSS utilizza un set di regole definito dall'amministratore per spostare i file utilizzati raramente nell'archiviazione a lungo termine, ad esempio un nastro o un supporto ottico. USA i reparse point per archiviare le informazioni relative al file nel file system. Queste informazioni vengono archiviate in un file stub contenente un punto di analisi i cui dati puntano al dispositivo in cui si trova il file effettivo. Il filtro file system può utilizzare queste informazioni per recuperare il file.

I reparse point vengono usati anche per implementare le cartelle montate. Per ulteriori informazioni, vedere [determinare se una directory è una cartella montata](determining-whether-a-directory-is-a-volume-mount-point.md).

Ai reparse point si applicano le restrizioni seguenti:

-   È possibile stabilire i reparse point per una directory, ma la directory deve essere vuota. In caso contrario, il file system NTFS non riesce a stabilire il reparse point. Non è inoltre possibile creare directory o file in una directory che contiene un reparse point.
-   I reparse point e gli attributi estesi si escludono a vicenda. Il file system NTFS non è in grado di creare un punto di analisi quando il file contiene attributi estesi e non può creare attributi estesi in un file che contiene un reparse point.
-   I dati di reparse point, inclusi il tag e il **GUID** facoltativo, non possono superare i 16 kilobyte. L'impostazione di un punto di analisi ha esito negativo se la quantità di dati da inserire nel punto di analisi supera questo limite.
-   È previsto un limite di 63 reparse point in un percorso specificato.

    **Windows Server 2003 e Windows XP:** È previsto un limite di 31 punti di analisi in un percorso specificato.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag di reparse point](reparse-point-tags.md)<br/>                                 | Ogni reparse point ha un Tag Identifier che consente di distinguere in modo efficiente tra i diversi tipi di punti di analisi, senza dover esaminare i dati definiti dall'utente nel reparse point.<br/> |
| [Operazioni di reparse point](reparse-point-operations.md)<br/>                     | Descrive le operazioni di reparse point che è possibile eseguire usando [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol).<br/>                                                                                       |
| [Reparse point e operazioni su file](reparse-points-and-file-operations.md)<br/> | Descrive il modo in cui i reparse point abilitano il comportamento file system che si riparte dal comportamento che la maggior parte degli sviluppatori Windows prevede<br/>                                                                                     |



 

 

