---
title: File di risposta
description: In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL del compilatore MIDL , file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9b4d079e92dff3c25f8a38c6c73073a548ea91
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387071"
---
# <a name="response-files"></a>File di risposta

In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti. Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL. A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file. Ciò può essere utile a causa di limitazioni dell'ambiente di compilazione o per praticità del processo di compilazione. È possibile specificare un file di risposta MIDL come:

**midl** **\@ filename**

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Specifica il nome del file di risposta. Il nome del file di risposta deve seguire immediatamente il carattere @ senza spazi vuoti tra il carattere @ e il nome del file di risposta.

</dd> </dl>

Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale posizione nella riga di comando MIDL. Ogni argomento in un file di risposta deve iniziare e terminare sulla stessa riga. Non è possibile usare il carattere barra rovesciata ( \\ ) per concatenare le righe.

MIDL supporta argomenti della riga di comando che includono uno o più file di risposta, combinati con altre opzioni della riga di comando:

**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**

Il compilatore MIDL non supporta i file di risposta annidati.

 

 




