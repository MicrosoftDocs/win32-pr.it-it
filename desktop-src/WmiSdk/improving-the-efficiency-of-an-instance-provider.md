---
description: Un provider WMI ad alte prestazioni aumenta notevolmente la velocità con cui un client WMI può ottenere informazioni da un provider di istanze WMI.
ms.assetid: 767a16bb-44b6-4c56-b79b-23241fcc216e
ms.tgt_platform: multiple
title: Miglioramento dell'efficienza di un provider di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d166cdc4817068363eec899a010c778b4fa125fbfb4eda11b2745558886be4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318815"
---
# <a name="improving-the-efficiency-of-an-instance-provider"></a>Miglioramento dell'efficienza di un provider di istanze

Un provider WMI ad alte prestazioni aumenta notevolmente la velocità con cui un client WMI può ottenere informazioni da un provider di istanze WMI. La modifica principale è che un provider ad alte prestazioni viene eseguito come server in-process per l'applicazione client o per WMI. Inserendo il provider all'interno del processo client, è possibile velocizzare l'interazione tra i due.

Per altre informazioni su come rendere il provider di istanza un provider ad alte prestazioni, vedere Creazione di un provider di istanze in un provider [High-Performance.](making-an-instance-provider-into-a-high-performance-provider.md)

 

 



