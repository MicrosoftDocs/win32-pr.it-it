---
description: Creazione di oggetti BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Creazione di oggetti BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304831"
---
# <a name="creating-byot-objects"></a>Creazione di oggetti BYOT

Un nuovo oggetto BYOT crea oggetti con transazioni manuali. Le due interfacce, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), hanno un solo metodo, **CreateInstance**, che accettano rispettivamente un puntatore all'interfaccia **ITransaction** e un URL del suggerimento. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) restituisce un puntatore di interfaccia all'oggetto appena creato, che viene integrato nella transazione specificata.

Quando viene rilasciato un oggetto con una transazione manuale, COM+ non tenta di eseguire il commit della transazione. La transazione viene controllata in modo esplicito dal gestore delle transazioni esterno che ha distribuito la transazione in cui è stato creato l'oggetto.

> [!Note]  
> È necessario importare l'oggetto BYOT. ByotServerEx in un'applicazione COM+.

 

 

 



