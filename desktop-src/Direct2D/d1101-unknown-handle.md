---
title: Handle sconosciuto d1101
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: È stata passata un'interfaccia non allocata da questa DLL.
keywords:
- D1101 handle Direct2D sconosciuto
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334282"
---
# <a name="d1101-unknown-handle"></a>D1101: handle sconosciuto

Un' \[ *interfaccia* \] di interfaccia non allocata da questa dll è stata passata.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possibili cause

Utilizzo di risorse non valido. La risorsa creata all'esterno di Direct2D viene usata con una factory Direct2D oppure le risorse create in una factory sono state usate con una risorsa creata da un'altra Factory.

 

 




