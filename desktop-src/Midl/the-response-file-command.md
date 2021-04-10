---
title: Comando del file di risposta
description: Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- riferimento alla riga di comando MIDL, comando del file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955718"
---
# <a name="the-response-file-command"></a>Comando del file di risposta

Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL. A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file. Questo può essere utile a causa delle limitazioni dell'ambiente di compilazione o per praticità per il processo di compilazione.

## <a name="switch-options"></a>Opzioni switch

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*file di risposta \_*
</dt> <dd>

Specifica il nome di un file di risposta. Il nome del file di risposta deve seguire immediatamente il carattere @. Non è consentito alcuno spazio vuoto tra il carattere @ e il nome del file di risposta.

</dd> </dl>

## <a name="remarks"></a>Commenti

In alternativa all'inserimento di tutte le opzioni associate a un commutatore nella riga di comando, il compilatore MIDL accetta i file di risposta che contengono opzioni e argomenti. Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale posizione nella riga di comando MIDL.

Ogni argomento in un file di risposta deve iniziare e terminare sulla stessa riga. Carattere barra rovesciata ( \) non può essere usato per concatenare le linee. Quando fa parte di una stringa racchiusa tra virgolette nel file di risposta, il carattere barra rovesciata può essere usato solo prima di un'altra barra rovesciata o prima di un carattere di virgolette doppie ("). Quando non fa parte di una stringa racchiusa tra virgolette, è possibile usare il carattere barra rovesciata solo prima di un carattere di virgolette doppie.

MIDL supporta gli argomenti della riga di comando che includono uno o più file di risposta combinati con altre opzioni della riga di comando.

Il compilatore MIDL non supporta i file di risposta annidati.

## <a name="examples"></a>Esempio

**MIDL @midl.rsp**

**MIDL-Oicf @midl1.rsp -ENV Win32 @midl2.rsp ITF. idl**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi della riga di comando MIDL generale](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




