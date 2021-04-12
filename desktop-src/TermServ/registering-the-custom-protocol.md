---
title: Registrazione di gestione protocolli
description: È necessario creare almeno una voce del valore del registro di sistema per gestione protocolli, in modo che il servizio Servizi Desktop remoto possa crearne un'istanza.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395623"
---
# <a name="registering-the-protocol-manager"></a><span data-ttu-id="f109f-103">Registrazione di gestione protocolli</span><span class="sxs-lookup"><span data-stu-id="f109f-103">Registering the Protocol Manager</span></span>

<span data-ttu-id="f109f-104">È necessario creare almeno una voce del valore del registro di sistema per gestione protocolli, in modo che il servizio Servizi Desktop remoto possa crearne un'istanza.</span><span class="sxs-lookup"><span data-stu-id="f109f-104">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

## <a name="registry-location"></a><span data-ttu-id="f109f-105">Percorso del registro</span><span class="sxs-lookup"><span data-stu-id="f109f-105">Registry Location</span></span>

<span data-ttu-id="f109f-106">Creare una chiave del registro di sistema nel percorso seguente per ogni listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) usato dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="f109f-106">Create a registry key in the following location for each listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) that your protocol uses.</span></span> <span data-ttu-id="f109f-107">In questo esempio le nuove chiavi del listener sono denominate *MyListener1* e *MyListener2*.</span><span class="sxs-lookup"><span data-stu-id="f109f-107">In this example, the new listener keys are called *MyListener1* and *MyListener2*.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

<span data-ttu-id="f109f-108">Come riferimento, è possibile visualizzare le voci di valore sotto la chiave del listener **RDP-TCP** predefinito in questo percorso.</span><span class="sxs-lookup"><span data-stu-id="f109f-108">For reference, you can view the value entries under the default **RDP-Tcp** listener key in this location.</span></span>

## <a name="registry-value-entries"></a><span data-ttu-id="f109f-109">Voci del valore del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f109f-109">Registry Value Entries</span></span>

<span data-ttu-id="f109f-110">La chiave del listener per il protocollo deve avere una voce di valore denominata **\_ oggetto LoadableProtocol**</span><span class="sxs-lookup"><span data-stu-id="f109f-110">The listener key for the protocol must have a value entry called **LoadableProtocol\_Object**</span></span><dl> <dt>

<span data-ttu-id="f109f-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f109f-111">Data type</span></span>
</dt> <dd><span data-ttu-id="f109f-112">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f109f-112">REG_SZ</span></span></dd> <span data-ttu-id="f109f-113">Interfaccia </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> .) Il servizio Servizi Desktop remoto utilizza questo CLSID per creare un'istanza del gestore di protocollo per questo listener dopo aver trovato il listener nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f109f-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> interface.) The Remote Desktop Services service uses this CLSID to instantiate the protocol manager for this listener after it finds the listener in the registry.</span></span>

<span data-ttu-id="f109f-114">Se il provider del protocollo usa più di un listener, il servizio Servizi Desktop remoto crea solo un'istanza di gestione protocolli e la usa per chiamare [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) una volta per ogni listener.</span><span class="sxs-lookup"><span data-stu-id="f109f-114">If your protocol provider uses more than one listener, the Remote Desktop Services service only creates one instance of the protocol manager, and uses it to call [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) once for each listener.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f109f-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f109f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f109f-116">Creazione di un provider di Remote Desktop Protocol</span><span class="sxs-lookup"><span data-stu-id="f109f-116">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="f109f-117">Sequenza di chiamate al metodo</span><span class="sxs-lookup"><span data-stu-id="f109f-117">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> </dl>

 

 




