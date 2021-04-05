---
title: Uso di Bluetooth
description: In questa sezione vengono descritte le attività correlate alla scrittura di applicazioni basate su Windows per Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734530"
---
# <a name="using-bluetooth"></a><span data-ttu-id="be4f6-103">Uso di Bluetooth</span><span class="sxs-lookup"><span data-stu-id="be4f6-103">Using Bluetooth</span></span>

<span data-ttu-id="be4f6-104">In questa sezione vengono descritte le attività correlate alla scrittura di applicazioni basate su Windows per Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="be4f6-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="be4f6-105">Bluetooth fornisce le definizioni di programmazione nei file Ws2bth. h e BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="be4f6-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="be4f6-106">Il file Bthsdpdef. h deve essere incluso prima di BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="be4f6-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="be4f6-107">Per usare i Socket Bluetooth, è necessario includere il file Ws2bth. h dopo Winsock2. h.</span><span class="sxs-lookup"><span data-stu-id="be4f6-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="be4f6-108">Collegare solo a bthprops. lib ed evitare il collegamento a irprops. lib.</span><span class="sxs-lookup"><span data-stu-id="be4f6-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="be4f6-109">Irprops. lib è disponibile solo per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="be4f6-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="be4f6-110">Bthprops. lib è disponibile in Windows Vista SDK.</span><span class="sxs-lookup"><span data-stu-id="be4f6-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="be4f6-111">È possibile utilizzare Windows Vista SDK per sviluppare applicazioni per Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="be4f6-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="be4f6-112">Windows Vista SDK è disponibile nell' [area download](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span><span class="sxs-lookup"><span data-stu-id="be4f6-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="be4f6-113">Tutti i meccanismi sincroni e sovrapposti standard per la lettura e la scrittura di dati attualmente supportati con altre famiglie di indirizzi funzionano correttamente anche con la \_ famiglia di indirizzi AF BTH.</span><span class="sxs-lookup"><span data-stu-id="be4f6-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="be4f6-114">Con l'SDK è incluso un codice di esempio che illustra una semplice applicazione Bluetooth che usa il protocollo Winsock 2,2 e RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="be4f6-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="be4f6-115">Il codice sorgente per l'esempio si trova nel percorso di installazione di SDK in C: \\ programmi \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="be4f6-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="be4f6-116">In questa sezione vengono descritti gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="be4f6-116">This section describes the following topics.</span></span>



| <span data-ttu-id="be4f6-117">Sezione</span><span class="sxs-lookup"><span data-stu-id="be4f6-117">Section</span></span>                                                                                      | <span data-ttu-id="be4f6-118">Content</span><span class="sxs-lookup"><span data-stu-id="be4f6-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="be4f6-119">Programmazione Bluetooth con Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="be4f6-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="be4f6-120">Viene illustrato come utilizzare le interfacce Windows Sockets per implementare una rete Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="be4f6-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




