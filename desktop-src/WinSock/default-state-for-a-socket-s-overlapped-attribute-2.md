---
description: La funzione socket ha creato socket con l'attributo Overlapped impostato per impostazione predefinita nel primo Wsock32.dll, la versione a 32 bit di Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Stato predefinito per l'attributo Overlapped di un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129203"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>Stato predefinito per l'attributo Overlapped di un socket

La funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ha creato socket con l'attributo Overlapped impostato per impostazione predefinita nel primo Wsock32.dll, la versione a 32 bit di Windows sockets 1,1. Per garantire la compatibilità con le implementazioni Wsock32.dll attualmente distribuite, questo continuerà a essere il caso anche per Windows Sockets 2. Ovvero nei socket di Windows Sockets 2 creati con la funzione **socket** avrà l'attributo Overlapped. Tuttavia, per essere più compatibili con il resto dell'API Windows, i socket creati con [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) non saranno, per impostazione predefinita, hanno l'attributo Overlapped. Questo attributo verrà applicato solo se \_ è impostato il bit del flag WSA \_ sovrapposto.

 

 



