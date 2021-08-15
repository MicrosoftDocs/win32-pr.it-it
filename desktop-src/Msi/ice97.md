---
description: ICE97 verifica che due componenti non isolano un componente condiviso nella stessa directory.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29575d533e945cef922110315cd3300f56fe62ae61b34c92de7175916e6657ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315241"
---
# <a name="ice97"></a>ICE97

ICE97 verifica che due componenti non isolano un componente condiviso nella stessa directory.

## <a name="result"></a>Risultato

ICE97 invia gli avvisi seguenti.



| Avviso ICE97                                                                                                                                                                    | Descrizione                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Questo componente 1 installa il componente condiviso nella stessa directory 2 di un altro componente, che interrompe le regole del componente se entrambi \[ \] i componenti \[ (o più) sono selezionati per \] l'installazione. | Due componenti non devono isolare un componente condiviso nella stessa directory. |



 

Ad esempio, Component1 e Component2, che condividono ComponentShared, vengono installati nella stessa directory. Entrambi specificano ComponentShared come componente isolato. A causa dell'isolamento, i file in ComponentShared vengono copiati due volte nel riferimento alla directory \_ per Component1 e Component2. I componenti hanno ora un conteggio dei riferimenti per la copia dei file. Si tratta di una violazione delle regole del componente installer. Se Component1 viene disinstallato, i file dei componenti isolati vengono rimossi e Component2 viene interrotto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



