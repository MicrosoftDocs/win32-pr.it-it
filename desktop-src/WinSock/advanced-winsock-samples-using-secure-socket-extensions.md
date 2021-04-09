---
description: Esempi avanzati di Winsock con estensioni Secure Socket
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Esempi avanzati di Winsock con estensioni Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966683"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="8c5c0-103">Esempi avanzati di Winsock con estensioni Secure Socket</span><span class="sxs-lookup"><span data-stu-id="8c5c0-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="8c5c0-104">Esempio di client e server TCP sicuro</span><span class="sxs-lookup"><span data-stu-id="8c5c0-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="8c5c0-105">Con il Software Development Kit (SDK) di Microsoft Windows è incluso un esempio Winsock più avanzato che illustra l'uso delle estensioni Secure Socket.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8c5c0-106">L'esempio include un client e un server TCP che si connettono in modo sicuro tramite Winsock e le estensioni Secure Socket.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="8c5c0-107">Per impostazione predefinita, il codice sorgente di esempio Winsock viene installato nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="8c5c0-108">*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ esempi \\ NetDs \\ Winsock*</span><span class="sxs-lookup"><span data-stu-id="8c5c0-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="8c5c0-109">Un esempio si trova nella cartella seguente:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="8c5c0-110">*securesocket*</span><span class="sxs-lookup"><span data-stu-id="8c5c0-110">*securesocket*</span></span>

<span data-ttu-id="8c5c0-111">Il codice di esempio viene suddiviso in directory separate, come descritto di seguito:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="8c5c0-112">stcpclient: cartella che contiene il codice client TCP protetto.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="8c5c0-113">stcpcommon: cartella che contiene il codice di libreria comune condiviso tra il client e il server TCP protetti.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="8c5c0-114">stcpserver: cartella che contiene il codice del server TCP protetto.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="8c5c0-115">Si noti che gli esempi devono essere eseguiti in due computer diversi che eseguono Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="8c5c0-116">Inoltre, è necessario eseguire il provisioning delle credenziali IPsec in entrambi i computer per la connessione perché l'esempio utilizza IPsec per la protezione del traffico.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="8c5c0-117">Per ulteriori informazioni sull'impostazione delle credenziali IPsec, consultare la documentazione sulla [configurazione IPSec](/windows/desktop/FWP/ipsec-configuration) .</span><span class="sxs-lookup"><span data-stu-id="8c5c0-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="8c5c0-118">La compilazione dell'esempio genererà due file eseguibili:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="8c5c0-119">*stcpclient.exe* e *stcpserver.exe*.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="8c5c0-120">Copiare *stcpclient.exe* nel computer a e copiare *stcpserver.exe* nel computer B. Nel computer B avviare il server TCP eseguendo il comando seguente in un prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="8c5c0-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="8c5c0-121">**stcpserver.exe**</span></span>

<span data-ttu-id="8c5c0-122">Per altre opzioni di utilizzo per il server, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="8c5c0-123">**stcpserver.exe/?**</span><span class="sxs-lookup"><span data-stu-id="8c5c0-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="8c5c0-124">Quindi, nel computer A, avviare il client TCP eseguendo il comando seguente in un prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="8c5c0-125">**stcpclient.exe <completo-DNS-Name-for-Machine-B>**</span><span class="sxs-lookup"><span data-stu-id="8c5c0-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="8c5c0-126">A questo punto la connessione deve essere stabilita in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="8c5c0-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="8c5c0-127">Eseguire il comando seguente per altre opzioni di utilizzo per il client:</span><span class="sxs-lookup"><span data-stu-id="8c5c0-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="8c5c0-128">**stcpclient.exe/?**</span><span class="sxs-lookup"><span data-stu-id="8c5c0-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c5c0-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8c5c0-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c5c0-130">Informazioni sulla piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="8c5c0-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="8c5c0-131">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="8c5c0-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="8c5c0-132">Configurazione IPsec</span><span class="sxs-lookup"><span data-stu-id="8c5c0-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="8c5c0-133">Funzioni IPsec</span><span class="sxs-lookup"><span data-stu-id="8c5c0-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="8c5c0-134">Uso delle estensioni Secure Socket</span><span class="sxs-lookup"><span data-stu-id="8c5c0-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="8c5c0-135">Security Support Provider Interface (SSPI)</span><span class="sxs-lookup"><span data-stu-id="8c5c0-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="8c5c0-136">Piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="8c5c0-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="8c5c0-137">Funzioni API della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="8c5c0-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="8c5c0-138">Estensioni Secure socket Winsock</span><span class="sxs-lookup"><span data-stu-id="8c5c0-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
