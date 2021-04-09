---
description: Come creare un'applicazione Windows Sockets (Winsock) di base.
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Creazione di un'applicazione Winsock di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129207"
---
# <a name="creating-a-basic-winsock-application"></a>Creazione di un'applicazione Winsock di base

**Per creare un'applicazione Winsock di base**

1.  Creare un nuovo progetto vuoto.
2.  Aggiungere un file di origine C++ vuoto al progetto.
3.  Verificare che l'ambiente di compilazione faccia riferimento alle directory include, lib e src del Software Development Kit (SDK) di Microsoft Windows o della precedente piattaforma Software Development Kit (SDK).
4.  Verificare che l'ambiente di compilazione sia collegato al file della libreria WinSock WS2 \_ 32. lib. Le applicazioni che utilizzano Winsock devono essere collegate al \_ file della libreria WS2 32. lib. Il \# commento pragma indica al linker che è necessario il file *WS2 \_ 32. lib* .
5.  Iniziare a programmare l'applicazione Winsock. Usare l'API Winsock includendo i file di intestazione di Winsock 2. Il file di intestazione *Winsock2. h* contiene la maggior parte delle funzioni, delle strutture e delle definizioni Winsock. Il file di intestazione *Ws2tcpip. h* contiene le definizioni introdotte nel documento di allegato WinSock 2 Protocol-Specific per TCP/IP che include funzioni e strutture più recenti utilizzate per recuperare gli indirizzi IP.
    > [!Note]  
    > Stdio. h viene utilizzato per l'input e l'output standard, in particolare la funzione **printf ()** .

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> Il file di intestazione *iphlpapi. h* è obbligatorio se un'applicazione usa le API helper IP. Quando il file di intestazione *iphlpapi. h* è obbligatorio, la \# riga di inclusione per il file di intestazione *Winsock2. h* deve essere posizionata prima della \# riga di inclusione per il file di intestazione *iphlpapi. h* .
>
> Il file di intestazione *Winsock2. h* include internamente gli elementi di base del file di intestazione di *Windows. h* , quindi non esiste in genere una \# riga di inclusione per il file di intestazione di *Windows. h* nelle applicazioni Winsock. Se \# è necessaria una riga di inclusione per il file di intestazione di *Windows. h* , questa operazione deve essere preceduta dalla macro per la \# definizione e la media di Win32 \_ \_ \_ . Per motivi cronologici, per impostazione predefinita l'intestazione *Windows. h* include il file di intestazione *Winsock. h* per Windows Sockets 1,1. Le dichiarazioni nel file di intestazione *Winsock. h* sono in conflitto con le dichiarazioni nel file di intestazione *Winsock2. h* richiesto da Windows Sockets 2,0. La \_ macro Win32 snello \_ e \_ media impedisce che *Winsock. h* venga incluso nell'intestazione *Windows. h* . Di seguito è riportato un esempio che illustra questo problema.

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



Passaggio successivo: [inizializzazione di Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Informazioni su server e client](about-clients-and-servers.md)
</dt> </dl>

 

 



