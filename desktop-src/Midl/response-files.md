---
title: File di risposta
description: In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL compilatore MIDL, file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2019
ms.locfileid: "104397030"
---
# <a name="response-files"></a>File di risposta

In alternativa all'inserimento di tutte le opzioni nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti. Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL. A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file. Questo può essere utile a causa delle limitazioni dell'ambiente di compilazione o per praticità per il processo di compilazione. È possibile specificare un file di risposta MIDL come:

 **\@ nome file** MIDL

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Specifica il nome del file di risposta. Il nome del file di risposta deve seguire immediatamente il carattere @ senza spazi vuoti tra il carattere @ e il nome del file di risposta.

</dd> </dl>

Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale posizione nella riga di comando MIDL. Ogni argomento in un file di risposta deve iniziare e terminare sulla stessa riga. Non è possibile usare il carattere barra rovesciata ( \) per concatenare le linee.

MIDL supporta gli argomenti della riga di comando che includono uno o più file di risposta, combinati con altre opzioni della riga di comando:

**MIDL-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**

Il compilatore MIDL non supporta i file di risposta annidati.

 

 




