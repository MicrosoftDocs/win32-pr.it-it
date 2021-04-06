---
title: IRootStorage-implementazione del file composto
description: L'implementazione del file composto di COM di IRootStorage consente di salvare i file in situazioni di memoria insufficiente o di spazio su disco insufficiente. Per informazioni sul comportamento di questa interfaccia, vedere IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714569"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage-implementazione del file composto

L'implementazione del file composto di COM di [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) consente di salvare i file in situazioni di memoria insufficiente o di spazio su disco insufficiente. Per informazioni sul comportamento di questa interfaccia, vedere **IRootStorage**.

## <a name="when-to-use"></a>Utilizzo

Usare l'implementazione fornita dal sistema di [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) solo per supportare il salvataggio di file in condizioni di memoria insufficiente.

## <a name="remarks"></a>Commenti

È possibile chiamare l'implementazione di COM di [**IRootStorage:: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) per eseguire una normale operazione di salvataggio in un altro file. Tuttavia, le applicazioni che eseguono questa operazione potrebbero non essere compatibili con le generazioni future di archiviazione COM. Per evitare questa possibilità, le applicazioni che eseguono un'operazione di salvataggio devono creare manualmente il secondo file composto e richiamare [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). Il metodo **IRootStorage:: SwitchToFile** deve essere usato solo in situazioni di emergenza (memoria insufficiente o spazio su disco).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




