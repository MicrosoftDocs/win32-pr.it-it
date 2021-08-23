---
title: Comando del file di risposta
description: Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- riferimento alla riga di comando MIDL , comando del file di risposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c40d8f4255b15a7b95b9bdca9e72ae2cba8e7ea1d42281f441326090a9529d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013529"
---
# <a name="the-response-file-command"></a>Comando del file di risposta

Un file di risposta è un file di testo contenente una o più opzioni della riga di comando del compilatore MIDL. A differenza di una riga di comando, un file di risposta consente più righe di opzioni e nomi di file. Ciò può essere utile a causa delle limitazioni dell'ambiente di compilazione o per comodità per il processo di compilazione.

## <a name="switch-options"></a>Opzioni switch

``` syntax
midl @response_file
```

<dl> <dt>

<span id="response_file"></span><span id="RESPONSE_FILE"></span>*file di \_ risposta*
</dt> <dd>

Specifica il nome di un file di risposta. Il nome del file di risposta deve seguire immediatamente il carattere @. Non sono consentiti spazi vuoti tra il carattere @ e il nome del file di risposta.

</dd> </dl>

## <a name="remarks"></a>Commenti

In alternativa all'inserimento di tutte le opzioni associate a un'opzione nella riga di comando, il compilatore MIDL accetta file di risposta contenenti opzioni e argomenti. Le opzioni in un file di risposta vengono interpretate come se fossero presenti in tale posizione nella riga di comando MIDL.

Ogni argomento in un file di risposta deve iniziare e terminare nella stessa riga. Il carattere barra rovesciata ( \\ ) non può essere usato per concatenare righe. Quando fa parte di una stringa tra virgolette nel file di risposta, il carattere barra rovesciata può essere usato solo prima di un'altra barra rovesciata o prima di un carattere virgolette doppie ("). Quando non fa parte di una stringa tra virgolette, il carattere barra rovesciata può essere usato solo prima di un carattere virgolette doppie.

MIDL supporta argomenti della riga di comando che includono uno o più file di risposta combinati con altre opzioni della riga di comando.

Il compilatore MIDL non supporta i file di risposta annidati.

## <a name="examples"></a>Esempio

**Midl @midl.rsp**

**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi generale della riga di comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




