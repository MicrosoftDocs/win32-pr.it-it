---
description: Creazione di oggetti BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Creazione di oggetti BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128764"
---
# <a name="creating-byot-objects"></a>Creazione di oggetti BYOT

Un nuovo oggetto BYOT crea oggetti con transazioni manuali. Le due [**interfacce, ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), hanno un solo metodo, **CreateInstance**, che accetta rispettivamente un puntatore a interfaccia **ITransaction** e un URL TIP. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) restituisce un puntatore a interfaccia all'oggetto appena creato, che viene incorporato nella transazione specificata.

Quando viene rilasciato un oggetto con una transazione manuale, COM+ non tenta di eseguire il commit della transazione. La transazione viene controllata in modo esplicito dal gestore delle transazioni esterno che ha dispensato la transazione in cui è stato creato l'oggetto.

> [!Note]  
> L'oggetto Byot.ByotServerEx deve essere importato in un'applicazione COM+.

 

 

 



