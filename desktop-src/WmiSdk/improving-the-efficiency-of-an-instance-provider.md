---
description: Un provider WMI a prestazioni elevate aumenta significativamente la velocità con cui un client WMI può ottenere informazioni da un provider di istanze WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Miglioramento dell'efficienza di un provider di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fecd0d8a20a3dcccd2878996823a7eb8a7ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883529"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a>Miglioramento dell'efficienza di un provider di istanze

Un provider WMI a prestazioni elevate aumenta significativamente la velocità con cui un client WMI può ottenere informazioni da un provider di istanze WMI. La modifica principale è che un provider a prestazioni elevate viene eseguito come server in-Process nell'applicazione client o in WMI. Inserendo il provider nel processo client, è possibile velocizzare l'interazione tra i due.

Per ulteriori informazioni su come rendere il provider di istanze un provider a prestazioni elevate, vedere Creazione di un [provider di istanze in un provider di High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).

 

 



