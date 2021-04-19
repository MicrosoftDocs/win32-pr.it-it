---
description: ICE97 verifica che due componenti non Isolino un componente condiviso nella stessa directory.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313814"
---
# <a name="ice97"></a>ICE97

ICE97 verifica che due componenti non Isolino un componente condiviso nella stessa directory.

## <a name="result"></a>Risultato

ICE97 invia gli avvisi seguenti.



| Avviso di ICE97                                                                                                                                                                    | Descrizione                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Questo componente \[ 1 \] installa il componente condiviso nella stessa directory \[ 2 \] di un altro, che interrompe le regole dei componenti se per l'installazione sono selezionati entrambi i componenti. | Due componenti non devono isolare un componente condiviso nella stessa directory. |



 

Ad esempio, Component1 e Component2, che condividono ComponentShared, vengono installati nella stessa directory. Entrambi specificano ComponentShared come componente isolato. A causa dell'isolamento, i file in ComponentShared vengono copiati due volte nel \_ riferimento alla directory per Component1 e Component2. Ai componenti è ora associato un conteggio dei riferimenti per la copia dei file. Questo problema si verifica in violazione delle regole dei componenti del programma di installazione. Se Component1 viene disinstallato, i file dei componenti isolati vengono rimossi e Component2 è danneggiato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



