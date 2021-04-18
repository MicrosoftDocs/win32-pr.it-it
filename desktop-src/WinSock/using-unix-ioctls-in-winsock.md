---
description: Il comando SIOCGIFCONF fornito dalla maggior parte delle implementazioni di UNIX è supportato sotto forma di funzioni WSAIoctl e WSPIoctl con il comando SIO \_ get \_ Interface \_ List. Questo comando restituisce l'elenco delle interfacce configurate e dei relativi parametri.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Uso di IOCTL UNIX in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313224"
---
# <a name="using-unix-ioctls-in-winsock"></a>Uso di IOCTL UNIX in Winsock

Il comando **SIOCGIFCONF** fornito dalla maggior parte delle implementazioni di UNIX è supportato sotto forma di funzioni [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) con il comando **sio \_ get \_ Interface \_ List**. Questo comando restituisce l'elenco delle interfacce configurate e dei relativi parametri.

> [!Note]  
> Il supporto di questo comando è obbligatorio per i provider di servizi TCP/IP conformi a Windows Sockets 2.

 

Il parametro *lpvOutBuffer* punta al buffer in cui [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) archiviano le informazioni sulle interfacce. Il numero di interfacce (numero di strutture restituite in *lpvOutBuffer*) può essere determinato in base alla lunghezza effettiva del buffer di output restituito in *lpcbBytesReturned*.

 

 
