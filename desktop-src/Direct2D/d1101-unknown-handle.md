---
title: Handle sconosciuto D1101
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: È stata passata un'interfaccia non allocata da questa DLL.
keywords:
- D1101 Handle sconosciuto Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161002"
---
# <a name="d1101-unknown-handle"></a>D1101: Handle sconosciuto

È stata \[ *passata* \] un'interfaccia di interfaccia non allocata da questa DLL.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possibili cause

Utilizzo delle risorse non valido. La risorsa creata all'esterno di Direct2D viene usata con una factory Direct2D oppure le risorse create in una factory sono state usate con una risorsa creata da un'altra factory.

 

 




