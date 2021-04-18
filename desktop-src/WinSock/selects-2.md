---
description: Nell'interfaccia socket originale di Berkeley Software Distribution (BSD) la funzione Select era lo standard (e solo) indica di ottenere le indicazioni relative agli eventi di rete.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Seleziona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e50339f298c18c75ad6451590f191fc1bd8afba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309936"
---
# <a name="selects"></a>Seleziona

Nell'interfaccia socket originale di Berkeley Software Distribution (BSD) la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era lo standard (e solo) indica di ottenere le indicazioni relative agli eventi di rete. Per ogni socket, è possibile eseguire il polling o l'attesa delle informazioni sullo stato di lettura, scrittura o errore. Per ulteriori informazioni, vedere [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) . Si noti che l'evento \_ di rete QoS FD non può essere ottenuto con questo approccio.

 

 
