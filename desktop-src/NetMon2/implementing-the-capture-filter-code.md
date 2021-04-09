---
description: Dopo aver determinato come organizzare il filtro tramite una struttura CAPTUREFILTER, è necessario allocare e compilare la struttura, che viene quindi passata al driver Network Monitor tramite un BLOB di configurazione.
ms.assetid: c2709da6-4d70-4abe-bab5-941053217e57
title: Implementazione del codice del filtro di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c407f3208a1c7720655667f78e4422b57882de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885848"
---
# <a name="implementing-the-capture-filter-code"></a>Implementazione del codice del filtro di acquisizione

Dopo aver determinato come organizzare il filtro tramite una struttura [**capturefilter**](capturefilter.md) , è necessario allocare e compilare la struttura, che viene quindi passata al driver Network Monitor tramite un BLOB di configurazione.

Gli utenti diretti di NPP aggiungono il filtro di acquisizione al BLOB di configurazione passato a **Connect**, [**Configure**](configure.md)o both. Per un elenco di interfacce COM che è possibile usare per comunicare con l'oggetto NPP, vedere [interfacce NPP](npp-interfaces.md).

 

 



