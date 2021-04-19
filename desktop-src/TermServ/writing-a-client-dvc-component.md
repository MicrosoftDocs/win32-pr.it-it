---
title: Scrittura di un modulo client DVC
description: Per scrivere un modulo client Dynamic Channel (DVC), è necessario innanzitutto implementare e registrare un plug-in client di Connessione Desktop remoto (RDC).
ms.assetid: b6f475d4-d2ad-41ce-b3b9-d844fbd23cf0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb881fd057132eb416066ffac050f75f4df1b12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298414"
---
# <a name="writing-a-client-dvc-module"></a><span data-ttu-id="ed3a4-103">Scrittura di un modulo client DVC</span><span class="sxs-lookup"><span data-stu-id="ed3a4-103">Writing a Client DVC Module</span></span>

<span data-ttu-id="ed3a4-104">Per scrivere un modulo client Dynamic Channel (DVC), è necessario innanzitutto implementare e registrare un plug-in client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="ed3a4-104">To write a dynamic virtual channel (DVC) client module, you must first implement and register a Remote Desktop Connection (RDC) client plug-in.</span></span> <span data-ttu-id="ed3a4-105">Il plug-in DVC è un'implementazione di [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registrato come oggetto Component Object Model (com).</span><span class="sxs-lookup"><span data-stu-id="ed3a4-105">The DVC plug-in is an implementation of [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin), registered as a Component Object Model (COM) object.</span></span>

> [!Note]  
> <span data-ttu-id="ed3a4-106">Il plug-in deve essere implementato in un modello a thread libero.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-106">The plug-in must be implemented in a free-threading model.</span></span> <span data-ttu-id="ed3a4-107">L'implementazione del modello di Apartment non è supportata.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-107">Apartment-model implementation is not supported.</span></span>

 

<span data-ttu-id="ed3a4-108">Di seguito è riportato un elenco di interfacce implementate da oggetti di cui viene creata un'istanza dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-108">The following is a list of interfaces that are implemented by objects that are instantiated by the plug-in.</span></span>



| <span data-ttu-id="ed3a4-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ed3a4-109">Interface</span></span>                                                        | <span data-ttu-id="ed3a4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed3a4-110">Description</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed3a4-111">**IWTSPlugin**</span><span class="sxs-lookup"><span data-stu-id="ed3a4-111">**IWTSPlugin**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin)                                 | <span data-ttu-id="ed3a4-112">Consente il caricamento del plug-in del client Connessione Desktop remoto (RDC) dal client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="ed3a4-112">Allows for the Remote Desktop Connection (RDC) client plug-in to be loaded by the Remote Desktop Connection (RDC) client.</span></span><br/>                                                                 |
| [<span data-ttu-id="ed3a4-113">**IWTSListenerCallback**</span><span class="sxs-lookup"><span data-stu-id="ed3a4-113">**IWTSListenerCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistenercallback)             | <span data-ttu-id="ed3a4-114">Notifica al plug-in del client Connessione Desktop remoto (RDC) informazioni sulle richieste in ingresso su un listener specifico.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-114">Notifies the Remote Desktop Connection (RDC) client plug-in about incoming requests on a particular listener.</span></span><br/>                                                                             |
| [<span data-ttu-id="ed3a4-115">**IWTSVirtualChannelCallback**</span><span class="sxs-lookup"><span data-stu-id="ed3a4-115">**IWTSVirtualChannelCallback**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelcallback) | <span data-ttu-id="ed3a4-116">Riceve le notifiche relative alle modifiche dello stato del canale o ai dati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-116">Receives notifications about channel state changes or data received.</span></span> <span data-ttu-id="ed3a4-117">Ogni istanza di questa interfaccia è associata a un'istanza di [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span><span class="sxs-lookup"><span data-stu-id="ed3a4-117">Each instance of this interface is associated with one instance of [**IWTSVirtualChannel**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel).</span></span><br/> |



 

<span data-ttu-id="ed3a4-118">Di seguito è riportato un elenco di interfacce implementate da oggetti di cui viene creata un'istanza dal client Connessione Desktop remoto (RDC) e che fanno parte del Framework.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-118">The following is a list of interfaces that are implemented by objects that are instantiated by the Remote Desktop Connection (RDC) client, and are part of the framework.</span></span>



| <span data-ttu-id="ed3a4-119">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="ed3a4-119">Interface</span></span>                                                      | <span data-ttu-id="ed3a4-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed3a4-120">Description</span></span>                                                                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed3a4-121">**IWTSVirtualChannelManager**</span><span class="sxs-lookup"><span data-stu-id="ed3a4-121">**IWTSVirtualChannelManager**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannelmanager) | <span data-ttu-id="ed3a4-122">Gestisce tutti i plug-in del client Connessione Desktop remoto (RDC), i listener DVC o i canali virtuali statici.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-122">Manages all Remote Desktop Connection (RDC) client plug-ins, DVC listeners, or static virtual channels.</span></span><br/> |
| [<span data-ttu-id="ed3a4-123">**IWTSListener**</span><span class="sxs-lookup"><span data-stu-id="ed3a4-123">**IWTSListener**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtslistener)                           | <span data-ttu-id="ed3a4-124">Gestisce le impostazioni di configurazione per ogni listener per la connessione DVC.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-124">Manages configuration settings for each listener for the DVC connection.</span></span><br/>                                |
| [<span data-ttu-id="ed3a4-125">**IWTSVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="ed3a4-125">**IWTSVirtualChannel**</span></span>](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsvirtualchannel)               | <span data-ttu-id="ed3a4-126">Controlla lo stato del canale, nonché le Scritture sul canale.</span><span class="sxs-lookup"><span data-stu-id="ed3a4-126">Controls the channel state, as well as writes on the channel.</span></span><br/>                                           |



 

<span data-ttu-id="ed3a4-127">Nella figura seguente viene illustrata la relazione tra il client di Connessione Desktop remoto (RDC) e il plug-in del client di Connessione Desktop remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="ed3a4-127">The following illustration shows the relationship between the Remote Desktop Connection (RDC) client and the Remote Desktop Connection (RDC) client plug-in.</span></span>

![relazione tra il client e il plug-in](images/tsclient.png)

 

 





