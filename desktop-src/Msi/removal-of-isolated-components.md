---
description: Windows Installer esegue le azioni seguenti durante la rimozione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.
ms.assetid: 26343a01-9a06-43d5-bbe3-959faf51739d
title: Rimozione di componenti isolati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf19769067230b82f68a35f7b9fbedcd1c56440
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314781"
---
# <a name="removal-of-isolated-components"></a>Rimozione di componenti isolati

Windows Installer esegue le azioni seguenti durante la rimozione di un'applicazione quando il pacchetto contiene componenti isolati. In genere, \_ il componente condiviso è una DLL condivisa dall' \_ applicazione componente e da altri eseguibili client.

## <a name="uninstall"></a>Disinstallare

-   Rimuovere i file di componente \_ condivisi dalla cartella contenente l' \_ applicazione Component solo se \_ viene rimossa anche l'applicazione componente.
-   Se il bit msidbComponentAttributesSharedDllRefCount è impostato nella [tabella dei componenti](component-table.md) , decrementare SHAREDDLL refcount.
-   Rimuovere il. File locale di zero byte dalla cartella contenente l' \_ applicazione componente.
-   Rimuovere \_ l'applicazione componente dall'elenco client di componenti \_ condivisi.
-   Rimuovere tutte le risorse dell'applicazione componente \_ come di consueto.

Se sono presenti altri prodotti rimanenti nell'elenco client di componenti \_ condivisi:

-   Rimuovere i file dal percorso condiviso del componente \_ condiviso.

Se il refcount SharedDLL per il componente \_ condiviso è 0 dopo essere stato decrementato oppure se non sono presenti altri client rimanenti del componente \_ condiviso:

-   Rimuovere i file di componente \_ condivisi dal percorso condiviso.
-   Elabora tutte le azioni di disinstallazione rispetto a questo componente.

 

 



