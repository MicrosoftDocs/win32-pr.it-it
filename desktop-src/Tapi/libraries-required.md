---
description: Di seguito è riportato un elenco di file lib necessari per compilare varie applicazioni TAPI 3, a data 22/1/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Librerie necessarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8337042681d84b5f93d5d0218cff18c4bef9259543f60fd13f692ebe5611835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621361"
---
# <a name="libraries-required"></a>Librerie necessarie

Elenco di file lib necessari per compilare varie applicazioni TAPI 3, a data 22/1/01:

-   Advapi32.lib
-   Amstrmid.lib (GUID ActiveMovie)
-   Kernel32.lib
-   Mdhcpid.lib (GUID multicast)
-   Ole32.lib (COM)
-   Oleaut32.lib (automazione COM)
-   Rendid.lib (GUID Rendezvous)
-   Rpcndr.lib
-   Rpcns4.lib
-   Rpcrt4.lib
-   Sdpblbid.lib (GUID SDP (Session Descriptor Protocol)
-   Strmiids.lib
-   User32.lib
-   Uuid.lib
-   Wldap32.lib
-   Ws2 \_ 32.lib

Se si usa Microsoft Visual Studio, potrebbe essere necessario aggiornare la versione. In particolare, Link.exe deve contenere una data del 19/3/98 o successiva.

Le definisce del compilatore devono includere WIN32 WINNT impostato su almeno 0x500 \_ \_ \_ win32 \_ DCOM.

 

 



