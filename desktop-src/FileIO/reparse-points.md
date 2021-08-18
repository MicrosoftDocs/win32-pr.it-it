---
description: Descrive i reparse point.
ms.assetid: 3abb3a08-9a00-43eb-9792-82eab1a25f06
title: Punti di analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d129036f954533134656afd02591eba68e3ecd9498de5aceea4b33fd750e786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015159"
---
# <a name="reparse-points"></a>Punti di analisi

Un file o una directory può contenere *un reparse point,* ovvero una raccolta di dati definiti dall'utente. Il formato di questi dati viene riconosciuto dall'applicazione che archivia i dati e da un filtro file system, installato per interpretare i dati ed elaborare il file. Quando un'applicazione imposta un reparse point, archivia questi dati, oltre a un *tag reparse*, che identifica in modo univoco i dati archiviati. Quando il file system apre un file con un reparse point, tenta di trovare il filtro file system associato al formato dati identificato dal tag reparse. Se viene file system un filtro, il filtro elabora il file come indicato dai dati di reparse. Se un filtro file system non viene trovato, l'operazione di apertura del file ha esito negativo.

Ad esempio, i reparse point vengono usati per implementare i collegamenti file system NTFS e Microsoft Remote Archiviazione Server (RSS). RSS usa un set di regole definito dall'amministratore per spostare i file usati raramente nell'archiviazione a lungo termine, ad esempio su nastro o su supporti ottici. Usa i reparse point per archiviare le informazioni sul file nel file system. Queste informazioni vengono archiviate in un file stub contenente un reparse point i cui dati puntano al dispositivo in cui si trova il file effettivo. Il file system filtro può usare queste informazioni per recuperare il file.

I reparse point vengono usati anche per implementare le cartelle montate. Per altre informazioni, vedere [Determinare se una directory è una cartella montata.](determining-whether-a-directory-is-a-volume-mount-point.md)

Ai reparse point si applicano le restrizioni seguenti:

-   È possibile stabilire reparse point per una directory, ma la directory deve essere vuota. In caso contrario, il file system NTFS non riesce a stabilire il reparse point. Inoltre, non è possibile creare directory o file in una directory che contiene un reparse point.
-   I reparse point e gli attributi estesi si escludono a vicenda. Il file system NTFS non può creare un reparse point quando il file contiene attributi estesi e non può creare attributi estesi in un file che contiene un reparse point.
-   I dati del reparse point, inclusi il tag e **il GUID facoltativo,** non possono superare i 16 kilobyte. L'impostazione di un reparse point ha esito negativo se la quantità di dati da inserire nel reparse point supera questo limite.
-   È previsto un limite di 63 reparse point in qualsiasi percorso specificato.

    **Windows Server 2003 e Windows XP:** È previsto un limite di 31 reparse point in qualsiasi percorso specificato.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tag dei punti di analisi](reparse-point-tags.md)<br/>                                 | Ogni reparse point ha un tag identificatore in modo che sia possibile distinguere in modo efficiente tra i diversi tipi di reparse point, senza dover esaminare i dati definiti dall'utente nel reparse point.<br/> |
| [Operazioni di reparse point](reparse-point-operations.md)<br/>                     | Vengono descritte le operazioni del reparse point che è possibile eseguire tramite [**DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)<br/>                                                                                       |
| [Reparse point e operazioni su file](reparse-points-and-file-operations.md)<br/> | Viene descritto in che modo i reparse point file system comportamento che si discosta dal comportamento previsto Windows gli sviluppatori.<br/>                                                                                     |



 

 

