---
title: Interoperabilità dei processi
description: È possibile eseguire applicazioni basate su Win32 in applicazioni a 64 bit Windows un livello di emulazione. Windows 10 arm include un livello di emulazione x86-on-ARM64. Per altre informazioni, vedere Esecuzione di applicazioni a 32 bit.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- interoperabilità dei processi a 64 bit Windows programmazione
- interoperabilità a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74e75af4299e9c249ea46b8eac2cdd47de10eb3f832aa88d6b313d20304afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561517"
---
# <a name="process-interoperability"></a>Interoperabilità dei processi

È possibile eseguire applicazioni basate su Win32 in applicazioni a 64 bit Windows un livello di emulazione. Windows 10 arm include un livello di emulazione x86-on-ARM64. Per altre informazioni, vedere [Esecuzione di applicazioni a 32 bit.](running-32-bit-applications.md)

Nelle librerie a 64 bit Windows un processo a 64 bit non può caricare una libreria a collegamento dinamico (DLL) a 32 bit. Inoltre, un processo a 32 bit non può caricare una DLL a 64 bit. Tuttavia, l'Windows a 64 bit supporta chiamate di procedura remota (RPC) tra processi a 64 bit e a 32 bit (sia nello stesso computer che tra computer). In un Windows a 64 bit un server COM out-of-process a 32 bit può comunicare con un client a 64 bit e un server COM out-of-process a 64 bit può comunicare con un client a 32 bit. Pertanto, se si dispone di una DLL a 32 bit che non supporta COM, è possibile eseguire il wrapping in un server COM out-of-process e usare COM per effettuare il marshalling delle chiamate da e verso un processo a 64 bit.

I server in-process sono attualmente registrati usando la **voce del Registro di sistema InprocServer.** Nei server in-process Windows a 64 bit, i server in-process a 64 e 32 bit devono usare la **voce InprocServer32.**

Per gli handle di porta, che per loro natura sono locali al computer e non verrebbero mai usati oltre il limite da 32 bit a 64 bit, usare il tipo **\_ HANDLE PTR** anziché il tipo **INT \_ PTR** o **DWORD \_ PTR.** Ciò include il porting di interfacce RPC che passano handle come **valori DWORD.** Handle **\_ PTR** a 64 bit è a 64 bit in transito (non troncato) e pertanto non richiede il mapping. **L'HANDLE \_ PTR a 32** bit è a 32 bit in transito.

Per altre informazioni, vedere Progettazione di interfacce compatibili [a 64 bit.](designing-64-bit-compatible-interfaces.md)

 

 




