---
description: Quando un file viene aperto da un processo che utilizza la funzione CreateFile, a esso viene associato un handle di file fino al termine del processo o alla chiusura dell'handle tramite la funzione CloseHandle.
ms.assetid: c8188e28-ec1b-4746-86f6-5996ff271677
title: Handle di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a54db1935108ab18666fb460a071d77c50f793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884889"
---
# <a name="file-handles"></a>Handle di file

Quando un file viene aperto da un processo che utilizza la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , a esso viene associato un *handle di file* fino al termine del processo o alla chiusura dell'handle tramite la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . L'handle di file viene usato per identificare il file in molte chiamate di funzione.

Ogni handle di file e oggetto file è in genere univoco per ogni processo che apre un file: le uniche eccezioni si verificano quando un handle di file utilizzato da un processo viene duplicato o quando un processo figlio eredita gli handle di file del processo padre. In queste situazioni, questi handle di file sono univoci, ma visualizzano un singolo oggetto file condiviso. Per ulteriori informazioni sulla duplicazione degli handle di file mantenuti dai processi, vedere [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .

Si noti che mentre gli handle di file sono in genere privati di un processo, i dati del file a cui il file fa riferimento non lo sono. Pertanto, i processi e i thread che condividono lo stesso file devono sincronizzarne l'accesso. Per la maggior parte delle operazioni su un file, un processo identifica il file tramite il pool di handle privato.

 

 
