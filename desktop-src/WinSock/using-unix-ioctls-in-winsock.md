---
description: Il comando SIOCGIFCONF fornito dalla maggior parte delle implementazioni UNIX è supportato sotto forma di funzioni WSAIoctl e WSPIoctl con il comando SIO \_ GET \_ INTERFACE \_ LIST. Questo comando restituisce l'elenco delle interfacce configurate e i relativi parametri.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Uso UNIX Ioctls in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558863"
---
# <a name="using-unix-ioctls-in-winsock"></a>Uso UNIX Ioctls in Winsock

Il **comando SIOCGIFCONF** fornito dalla maggior parte delle implementazioni UNIX è supportato sotto forma di funzioni [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) con il comando **SIO GET INTERFACE \_ \_ \_ LIST**. Questo comando restituisce l'elenco delle interfacce configurate e i relativi parametri.

> [!Note]  
> Il supporto di questo comando è obbligatorio Windows provider di servizi TCP/IP conformi a Sockets 2.

 

Il parametro *lpvOutBuffer* punta al buffer in cui [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) archiviano le informazioni sulle interfacce. Il numero di interfacce (numero di strutture restituite in *lpvOutBuffer*) può essere determinato in base alla lunghezza effettiva del buffer di output restituito in *lpcbBytesReturned.*

 

 
