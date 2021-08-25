---
description: Come creare un'applicazione Windows Sockets (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Creazione di un'applicazione Winsock di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b13acc0ae80242fb747415d457e6809895c38cd81878224cad2ffe130b2536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860951"
---
# <a name="creating-a-basic-winsock-application"></a>Creazione di un'applicazione Winsock di base

**Per creare un'applicazione Winsock di base**

1.  Creare un nuovo progetto vuoto.
2.  Aggiungere un file di origine C++ vuoto al progetto.
3.  Assicurarsi che l'ambiente di compilazione faccia riferimento alle directory Include, Lib e Src di Microsoft Windows Software Development Kit (SDK) o platform Software Development Kit (SDK) precedente.
4.  Assicurarsi che l'ambiente di compilazione sia collegata al file della libreria Winsock Ws2 \_ 32.lib. Le applicazioni che usano Winsock devono essere collegate al file di libreria Ws2 \_ 32.lib. Il commento pragma indica al linker che è necessario il \# file *Ws2 \_ 32.lib.*
5.  Iniziare a programmare l'applicazione Winsock. Usare l'API Winsock includendo i file di intestazione winsock 2. Il file *di intestazione Winsock2.h* contiene la maggior parte delle funzioni, delle strutture e delle definizioni di Winsock. Il file di intestazione *Ws2tcpip.h* contiene le definizioni introdotte nel documento Annex di WinSock 2 Protocol-Specific per TCP/IP che include le funzioni e le strutture più recenti usate per recuperare gli indirizzi IP.
    > [!Note]  
    > Stdio.h viene usato per l'input e l'output standard, in particolare la **funzione printf().**

     


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
> Il file *di intestazione Iphlpapi.h* è obbligatorio se un'applicazione usa le API helper IP. Quando il file di intestazione *Iphlpapi.h* è obbligatorio, la riga di inclusione per il file di intestazione Winsock2.h deve essere posizionata prima della riga di inclusione per il file di intestazione \#  \# *Iphlpapi.h.*
>
> Il file di *intestazione Winsock2.h* include internamente elementi di base del file di intestazione *Windows.h,* pertanto non è in genere presente una riga di inclusione per il file di intestazione \# *Windows.h* nelle applicazioni Winsock. Se è necessaria una riga di inclusione per il file di intestazione \# *Windows.h,* deve essere preceduta dalla \# macro DEFINE WIN32 \_ LEAN AND \_ \_ MEAN. Per motivi cronologici, *l'intestazione Windows.h* include per impostazione predefinita il file di *intestazione Winsock.h* per Windows Sockets 1.1. Le dichiarazioni nel file di intestazione *Winsock.h* saranno in conflitto con le dichiarazioni nel file di intestazione *Winsock2.h* richiesto da Windows Sockets 2.0. La macro WIN32 LEAN AND MEAN impedisce \_ \_ che \_ *Winsock.h* venga incluso *dall'intestazione Windows.h.* Di seguito è riportato un esempio che illustra questa operazione.

 


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



Passaggio successivo: [Inizializzazione di Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Informazioni su server e client](about-clients-and-servers.md)
</dt> </dl>

 

 



