---
title: Violazione Threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Un'interfaccia a thread di noleggio è stata accessibile simultaneamente da più thread.
keywords:
- Direct2D violazione Threading D1105
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/27/2021
ms.locfileid: "106334280"
---
# <a name="d1105-threading-violation"></a>D1105: violazione Threading

Un'interfaccia di interfaccia a thread \[  \] di noleggio è stata accessibile simultaneamente da più thread.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interfaccia*
</dt> <dd>

Indirizzo dell'interfaccia accessibile da più thread.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possibili cause

Uso di un'istanza di oggetto dalla stessa Factory a thread singolo da due thread diversi.

 

 




