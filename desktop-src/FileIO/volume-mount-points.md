---
description: Con le cartelle montate è possibile unificare diversi file System, ad esempio NTFS file system, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un file system logico in un singolo volume NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313871"
---
# <a name="mounted-folders"></a>Cartelle montate

Il file system NTFS supporta le cartelle montate. Una *cartella montata* è un'associazione tra un volume e una directory in un altro volume. Quando viene creata una cartella montata, gli utenti e le applicazioni possono accedere al volume di destinazione usando il percorso della cartella montata o la lettera di unità del volume. Ad esempio, un utente può creare una cartella montata per associare l'unità D: con la \\ cartella c: mnt \\ DDrive nell'unità C. Dopo aver creato la cartella montata, l'utente può usare il percorso "C: \\ mnt \\ DDrive" per accedere all'unità D: come se fosse una cartella nell'unità C:.

Con le cartelle montate è possibile unificare diversi file System, ad esempio NTFS file system, un file system FAT a 16 bit e un file system ISO-9660 in un'unità CD-ROM in un file system logico in un singolo volume NTFS. Né gli utenti né le applicazioni necessitano di informazioni sul volume di destinazione in cui si trova un file specifico. Tutte le informazioni necessarie per individuare un file specificato sono un percorso completo utilizzando una cartella montata nel volume NTFS. I volumi possono essere ridisposti, sostituiti o suddivisi in molti volumi senza che utenti o applicazioni debbano modificare le impostazioni.

Per informazioni sulle cartelle montate, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                         | Descrizione                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creazione di cartelle montate](mounting-and-dismounting-a-volume.md)<br/>                                                  | La creazione di una cartella montata è un processo in due passaggi.<br/>                                                                                                                                                                 |
| [Enumerazione di cartelle montate](enumerating-volume-mount-points.md)<br/>                                                 | Funzioni da utilizzare per enumerare le cartelle montate in un volume.<br/>                                                                                                                                                       |
| [Determinare se una directory è una cartella montata](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | Come determinare se una directory specificata è una cartella montata.<br/>                                                                                                                                              |
| [Assegnazione di una lettera di unità a un volume](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | È possibile assegnare una lettera di unità (ad esempio, X: \) a un volume locale usando la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , a condizione che non sia già stato assegnato un volume a tale lettera di unità.<br/> |
| [Funzioni cartella montata](volume-mount-point-functions.md)<br/>                                                       | Funzioni utilizzate per gestire le cartelle montate.<br/>                                                                                                                                                                        |



 

Per esempi, vedere [esempi di cartelle montate](volume-mount-point-examples.md).

 

 




