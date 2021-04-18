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
# <a name="process-interoperability"></a><span data-ttu-id="3d754-107">Interoperabilità del processo</span><span class="sxs-lookup"><span data-stu-id="3d754-107">Process Interoperability</span></span>

<span data-ttu-id="3d754-108">È possibile eseguire applicazioni basate su Win32 in Windows a 64 bit usando un livello di emulazione.</span><span class="sxs-lookup"><span data-stu-id="3d754-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="3d754-109">Windows 10 su ARM include un livello di emulazione x86-on-ARM64.</span><span class="sxs-lookup"><span data-stu-id="3d754-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="3d754-110">Per ulteriori informazioni, vedere [esecuzione di applicazioni a 32 bit](running-32-bit-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3d754-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="3d754-111">In Windows a 64 bit un processo a 64 bit non è in grado di caricare una libreria di collegamento dinamico (DLL) a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3d754-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="3d754-112">Inoltre, un processo a 32 bit non può caricare una DLL a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="3d754-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="3d754-113">Tuttavia, Windows a 64 bit supporta le chiamate di procedura remota (RPC) tra i processi a 64 e 32 bit (sia nello stesso computer che tra più computer).</span><span class="sxs-lookup"><span data-stu-id="3d754-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="3d754-114">In Windows a 64 bit, un server COM a 32 bit out-of-process può comunicare con un client a 64 bit e un server COM a 64 bit out-of-process può comunicare con un client a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3d754-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="3d754-115">Se pertanto si dispone di una DLL a 32 bit non compatibile con COM, è possibile eseguirne il wrapping in un server COM out-of-process e utilizzare COM per effettuare il marshalling delle chiamate da e verso un processo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="3d754-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="3d754-116">I server in-process sono attualmente registrati usando la voce del registro di sistema **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="3d754-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="3d754-117">Nei server Windows a 64 bit, 64 e 32 bit in-process devono usare la voce **InprocServer32** .</span><span class="sxs-lookup"><span data-stu-id="3d754-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="3d754-118">Per gli handle di porta, che per loro natura sono locali rispetto al computer e non vengono mai usati tra i limiti a 32 bit a 64 bit, usare il tipo di **handle \_ ptr** invece del tipo **int \_ ptr** o **DWORD \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="3d754-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="3d754-119">Sono incluse le interfacce RPC di porting che passano tali handle come valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3d754-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="3d754-120">Il **\_ ptr dell'HANDLE** a 64 bit è 64 bit sulla rete (non troncato) e pertanto non è necessario eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="3d754-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="3d754-121">(Il **\_ ptr dell'HANDLE** a 32 bit è 32 bit sulla rete).</span><span class="sxs-lookup"><span data-stu-id="3d754-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="3d754-122">Per altre informazioni, vedere [progettazione di interfacce compatibili con 64 bit](designing-64-bit-compatible-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="3d754-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




