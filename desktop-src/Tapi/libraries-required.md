---
description: Di seguito è riportato un elenco di file con estensione LIB necessari per compilare varie applicazioni TAPI 3, a partire da 1/22/01.
ms.assetid: f1765829-9a5d-4e85-b898-6679279aa6d9
title: Librerie richieste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0948599041c466a337d2d6828750a9996dc8d813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308298"
---
# <a name="libraries-required"></a>Librerie richieste

Elenco di file con estensione LIB necessari per compilare varie applicazioni TAPI 3, a partire da 1/22/01:

-   Advapi32. lib
-   Amstrmid. lib (GUID ActiveMovie)
-   Kernel32.lib
-   Mdhcpid. lib (GUID multicast)
-   Ole32. lib (COM)
-   Oleaut32. lib (automazione COM)
-   Rendid. lib (GUID Rendezvous)
-   Rpcndr. lib
-   Rpcns4. lib
-   Rpcrt4. lib
-   Sdpblbid. lib (GUID di Session Descriptor Protocol)
-   Strmiids. lib
-   User32. lib
-   UUID. lib
-   Wldap32. lib
-   WS2 \_ 32. lib

Se si usa Microsoft Visual Studio, potrebbe essere necessario aggiornare la versione. In particolare, Link.exe deve contenere una data di 3/19/98 o successiva.

Le definizioni del compilatore devono includere l' \_ \_ impostazione Win32 WinNT su almeno 0x500 e \_ Win32 \_ DCOM.

 

 



