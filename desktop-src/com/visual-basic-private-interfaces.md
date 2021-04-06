---
title: Interfacce private Visual Basic
description: Interfacce private Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045360"
---
# <a name="visual-basic-private-interfaces"></a>Interfacce private Visual Basic

In questa sezione vengono identificate due interfacce implementate da Visual Basic per le categorie di componenti. Non è previsto che i controlli richiedano queste categorie perché è possibile che i controlli offrano funzionalità alternative quando questi non sono disponibili.

L'interfaccia [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) consente ai controlli di integrarsi meglio nell'ambiente Visual Basic durante la formattazione dei dati.

CATId-{02496840-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBFormat

L'interfaccia [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) consente a un controllo di enumerare altri controlli nel form VB.

CATId-{02496841-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBGetControl

Di seguito sono descritte due interfacce private aggiuntive, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), anche se non definiscono le categorie di componenti. Non è consigliabile usare queste quattro interfacce perché non sono supportate da contenitori diversi da Visual Basic.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Categorie di componenti](component-categories.md)
</dt> </dl>

 

 




