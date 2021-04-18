---
title: Interoperabilità del processo
description: È possibile eseguire applicazioni basate su Win32 in Windows a 64 bit usando un livello di emulazione. Windows 10 su ARM include un livello di emulazione x86-on-ARM64. Per ulteriori informazioni, vedere esecuzione di applicazioni a 32 bit.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- elaborazione della programmazione Windows a 64 bit per l'interoperabilità
- interoperabilità per la programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298381"
---
# <a name="process-interoperability"></a>Interoperabilità del processo

È possibile eseguire applicazioni basate su Win32 in Windows a 64 bit usando un livello di emulazione. Windows 10 su ARM include un livello di emulazione x86-on-ARM64. Per ulteriori informazioni, vedere [esecuzione di applicazioni a 32 bit](running-32-bit-applications.md).

In Windows a 64 bit un processo a 64 bit non è in grado di caricare una libreria di collegamento dinamico (DLL) a 32 bit. Inoltre, un processo a 32 bit non può caricare una DLL a 64 bit. Tuttavia, Windows a 64 bit supporta le chiamate di procedura remota (RPC) tra i processi a 64 e 32 bit (sia nello stesso computer che tra più computer). In Windows a 64 bit, un server COM a 32 bit out-of-process può comunicare con un client a 64 bit e un server COM a 64 bit out-of-process può comunicare con un client a 32 bit. Se pertanto si dispone di una DLL a 32 bit non compatibile con COM, è possibile eseguirne il wrapping in un server COM out-of-process e utilizzare COM per effettuare il marshalling delle chiamate da e verso un processo a 64 bit.

I server in-process sono attualmente registrati usando la voce del registro di sistema **InprocServer** . Nei server Windows a 64 bit, 64 e 32 bit in-process devono usare la voce **InprocServer32** .

Per gli handle di porta, che per loro natura sono locali rispetto al computer e non vengono mai usati tra i limiti a 32 bit a 64 bit, usare il tipo di **handle \_ ptr** invece del tipo **int \_ ptr** o **DWORD \_ ptr** . Sono incluse le interfacce RPC di porting che passano tali handle come valori **DWORD** . Il **\_ ptr dell'HANDLE** a 64 bit è 64 bit sulla rete (non troncato) e pertanto non è necessario eseguire il mapping. (Il **\_ ptr dell'HANDLE** a 32 bit è 32 bit sulla rete).

Per altre informazioni, vedere [progettazione di interfacce compatibili con 64 bit](designing-64-bit-compatible-interfaces.md).

 

 




