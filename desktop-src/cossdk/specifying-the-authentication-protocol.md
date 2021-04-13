---
description: Specifica del protocollo di autenticazione
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Specifica del protocollo di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483421"
---
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="423b1-103">Specifica del protocollo di autenticazione</span><span class="sxs-lookup"><span data-stu-id="423b1-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="423b1-104">A seconda dei requisiti di sicurezza nel sito, è possibile richiedere che il servizio componenti in coda verifichi sempre l'identità di un client, non per verificare mai l'identità di un client o per verificare l'identità di un client solo se il componente è configurato per richiedere l'autenticazione anche quando non è possibile accedervi tramite una coda.</span><span class="sxs-lookup"><span data-stu-id="423b1-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="423b1-105">Per utilizzare un componente in coda in modalità gruppo di lavoro, il livello di autenticazione deve essere impostato su nessuno.</span><span class="sxs-lookup"><span data-stu-id="423b1-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="423b1-106">Strumento di amministrazione Servizi componenti</span><span class="sxs-lookup"><span data-stu-id="423b1-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="423b1-107">Per specificare il protocollo di autenticazione, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="423b1-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="423b1-108">Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="423b1-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="423b1-109">Fare clic con il pulsante destro del mouse sull'applicazione in coda per la quale si desidera specificare il protocollo di autenticazione, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="423b1-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="423b1-110">Selezionare la scheda **Accodamento** nella finestra di dialogo Proprietà.</span><span class="sxs-lookup"><span data-stu-id="423b1-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="423b1-111">In **autenticazione messaggi MSMQ** selezionare il pulsante di opzione associato al protocollo di autenticazione che si desidera implementare.</span><span class="sxs-lookup"><span data-stu-id="423b1-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="423b1-112">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="423b1-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="423b1-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="423b1-113">Visual Basic</span></span>

<span data-ttu-id="423b1-114">Usare il parametro *AUTHLEVEL* quando si attiva l'applicazione in coda come descritto in [uso del moniker della coda](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="423b1-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="423b1-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="423b1-115">C/C++</span></span>

<span data-ttu-id="423b1-116">Usare il parametro *AUTHLEVEL* quando si attiva l'applicazione in coda come descritto in [uso del moniker della coda](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="423b1-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="423b1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="423b1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="423b1-118">Sicurezza dei componenti in coda</span><span class="sxs-lookup"><span data-stu-id="423b1-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="423b1-119">Limitazioni di sicurezza in modalità gruppo di lavoro</span><span class="sxs-lookup"><span data-stu-id="423b1-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



