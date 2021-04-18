---
title: Glossario Gestione remota Windows
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321093"
---
# <a name="windows-remote-management-glossary"></a><span data-ttu-id="fc4d6-103">Glossario Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="fc4d6-103">Windows Remote Management Glossary</span></span>


<dl> <dt>

<span data-ttu-id="fc4d6-104">WSMan: elementi \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="fc4d6-104">\*\*\*\*wsman:Items\*\*\*\*</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-105">Un WS-Management elemento del protocollo restituito in un'enumerazione che ottiene sia le istanze di che l'istanza di [*EPRs*](/windows).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-105">A WS-Management protocol element returned in an enumeration that obtains both the instances and the instance [*EPRs*](/windows).</span></span> <span data-ttu-id="fc4d6-106">**WSMan: gli elementi** sono un contenitore che include un'istanza di e il relativo EPR.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-106">**wsman:Items** is a container that holds an instance and its EPR.</span></span> <span data-ttu-id="fc4d6-107">Questo tipo di enumerazione viene avviato quando il flag **WSManFlagReturnObjectAndEPR** viene impostato nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-107">This type of enumeration is initiated when the **WSManFlagReturnObjectAndEPR** flag is set in the request.</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="fc4d6-108">B</span><span class="sxs-lookup"><span data-stu-id="fc4d6-108">B</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-109">**Baseboard Management Controller (BMC)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-109">**baseboard management controller (BMC)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-110">Un microcontroller collegato localmente a un server.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-110">A microcontroller attached locally to a server.</span></span> <span data-ttu-id="fc4d6-111">BMC hanno sensori che monitorano lo stato fisico del server e una connessione di rete separata in grado di comunicare in rete, anche se il server è offline.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-111">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="fc4d6-112">È possibile accedere ai dati BMC tramite il provider WMI [*IPMI (Intelligent Platform Management Interface)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-112">You have access to BMC data through the [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-113">**Autenticazione di base**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-113">**Basic authentication**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-114">Nome utente e password inviati nello scambio di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-114">The user name and password sent in the authentication exchange.</span></span> <span data-ttu-id="fc4d6-115">L'autenticazione di base può essere configurata in modo da utilizzare il trasporto HTTP o HTTPS in un dominio o un gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-115">Basic authentication can be configured to use either HTTP or HTTPS transport in a domain or workgroup.</span></span> <span data-ttu-id="fc4d6-116">Si tratta del metodo di autenticazione meno sicuro.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-116">This method is the least secure method of authentication.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-117">**Baseboard Management Controller (BMC)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-117">**BMC**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-118">Vedere [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-118">See [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="fc4d6-119">C</span><span class="sxs-lookup"><span data-stu-id="fc4d6-119">C</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-120">**CIM**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-120">**CIM**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-121">Vedere [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-121">See [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-122">**client**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-122">**client**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-123">Applicazione client che utilizza il protocollo WS-Management per accedere al servizio di gestione nel computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-123">The client application using the WS-Management protocol to access the management service on either the local or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-124">**Common Information Model (CIM)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-124">**Common Information Model (CIM)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-125">Modello [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) che descrive come rappresentare oggetti di rete e computer reali.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-125">The [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md) model that describes how to represent real-world computer and network objects.</span></span> <span data-ttu-id="fc4d6-126">CIM utilizza un paradigma orientato agli oggetti, in cui gli oggetti gestiti vengono modellati mediante i concetti di classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-126">CIM uses an object-oriented paradigm, where managed objects are modeled using the concepts of classes and instances.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="fc4d6-127">D</span><span class="sxs-lookup"><span data-stu-id="fc4d6-127">D</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-128">**Autenticazione del digest**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-128">**Digest authentication**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-129">Uno scambio in cui il server riceve una richiesta da un client e invia i dati sul client a un server di autenticazione, in genere un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-129">An exchange wherein the server receives a request from a client and sends data about the client to an authenticating server, typically a domain controller.</span></span> <span data-ttu-id="fc4d6-130">Se il client viene autenticato, il server riceve una chiave di sessione digest utilizzata per autenticare le richieste successive dal client.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-130">If the client is authenticated, then the server receives a Digest session key used to authenticate subsequent requests from the client.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-131">**Distributed Management Task Force (DMTF)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-131">**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-132">Organizzazione del settore che sviluppa gli standard di gestione e la tecnologia di integrazione per ambienti aziendali e Internet.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-132">The industry organization developing management standards and integration technology for enterprise and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-133">**DMTF**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-133">**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-134">Vedere [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-134">See [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="fc4d6-135">E</span><span class="sxs-lookup"><span data-stu-id="fc4d6-135">E</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-136">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-136">**endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-137">Risorsa che può essere risolta da un [*riferimento all'endpoint (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-137">A resource that can be addressed by an [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-138">**riferimento endpoint (EPR)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-138">**endpoint reference (EPR)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-139">Combinazione di WS-Addressing e WS-Management che indirizzano elementi che insieme descrivono un indirizzo per una risorsa nell'intestazione SOAP del messaggio.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-139">A combination of WS-Addressing and WS-Management addressing elements that together describe an address for a resource in the message SOAP header.</span></span> <span data-ttu-id="fc4d6-140">Si tratta di un termine di servizio Web.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-140">This is a web service term.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-141">**enumeration**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-141">**enumeration**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-142">Set, o raccolta, di istanze di [*risorse*](windows-remote-management-glossary.md) o dell'azione di richiesta di tale set.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-142">A set, or collection, of [*resource*](windows-remote-management-glossary.md) instances or the action of requesting such a set.</span></span> <span data-ttu-id="fc4d6-143">In WS-Management protocollo, per ottenere la raccolta viene usato [*WS-Enumeration*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-143">In WS-Management protocol, [*WS-Enumeration*](windows-remote-management-glossary.md) is used to obtain the collection.</span></span> <span data-ttu-id="fc4d6-144">Nell'implementazione di scripting del servizio WinRM di Enumeration vengono usati [**Session. enumerate**](session-enumerate.md) e l'oggetto [**enumeratore**](enumerator.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-144">In the WinRM service scripting implementation of enumeration, [**Session.Enumerate**](session-enumerate.md) and the [**Enumerator**](enumerator.md) object are used.</span></span> <span data-ttu-id="fc4d6-145">Il metodo e l'interfaccia C++ corrispondenti sono [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) e [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-145">The corresponding C++ method and interface are [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) and [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-146">**EPR**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-146">**EPR**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-147">Vedere [*riferimento endpoint (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-147">See [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-148">**Servizio raccolta eventi**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-148">**Event Collection Service**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-149">Componente del sistema operativo che riceve gli eventi dal BMC e da altri componenti o applicazioni del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-149">The operating system component that receives events from the BMC and other operating system components or applications.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-150">**invio di eventi**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-150">**event forwarding**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-151">Una notifica degli eventi che si verificano in computer remoti può essere inviata alle applicazioni di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-151">A notification of events that occur on remote computers can be sent to subscribing applications.</span></span> <span data-ttu-id="fc4d6-152">L'invio di eventi non è una funzionalità di WinRM, ma del [registro eventi di Windows](/windows/desktop/WES/windows-event-log).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-152">Event forwarding is not a feature of WinRM, but of the [Windows Event Log](/windows/desktop/WES/windows-event-log).</span></span> <span data-ttu-id="fc4d6-153">L'invio di eventi diventa disponibile per la prima volta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-153">Event forwarding becomes available for the first time in Windows Vista.</span></span> <span data-ttu-id="fc4d6-154">Le applicazioni di gestione, ad esempio Microsoft Operations Manager (MOM) usano l'invio di eventi.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-154">The Management applications, such as Microsoft Operations Manager (MOM) use event forwarding.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="fc4d6-155">F</span><span class="sxs-lookup"><span data-stu-id="fc4d6-155">F</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-156">**filter**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-156">**filter**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-157">Meccanismo di query per specificare un set limitato di istanze nella richiesta di una [*risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-157">A query mechanism for specifying a limited set of instances in the request for a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-158">È possibile specificare un parametro di *filtro* per le chiamate a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-158">You can specify a *filter* parameter on calls to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-159">**dialetto filtro**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-159">**filter dialect**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-160">Stringa XML che identifica il dialetto XML utilizzato per specificare un [*filtro*](windows-remote-management-glossary.md) in una chiamata a [**Session. enumerate**](session-enumerate.md) o [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-160">An XML string that identifies the XML dialect used to specify a [*filter*](windows-remote-management-glossary.md) in a call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span> <span data-ttu-id="fc4d6-161">Il servizio gestione remota Windows supporta [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) come dialetto di filtro durante la ricezione di richieste.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-161">The WinRM service supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as a filter dialect when receiving requests.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-162">**frammento**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-162">**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-163">Stringa XML che identifica parte di un'istanza di una risorsa anziché l'intera risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-163">An XML string that identifies part of an instance of a resource rather than the entire resource.</span></span> <span data-ttu-id="fc4d6-164">Il supporto del frammento è disponibile nell'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-164">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-165">**dialetto frammento**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-165">**fragment dialect**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-166">Stringa XML che identifica il dialetto XML utilizzato per specificare un [*frammento*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-166">An XML string that identifies the XML dialect used to specify a [*fragment*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-167">Il supporto del frammento è disponibile nell'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-167">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="fc4d6-168">Il servizio WinRM supporta [*XPath*](windows-remote-management-glossary.md) per il dialetto Fragment durante la ricezione di richieste.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-168">The WinRM service supports [*XPath*](windows-remote-management-glossary.md) for fragment dialect when receiving requests.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="fc4d6-169">I</span><span class="sxs-lookup"><span data-stu-id="fc4d6-169">I</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-170">**in banda**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-170">**in-band**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-171">L'applicazione client ottiene i dati BMC tramite il [*listener*](windows-remote-management-glossary.md) WinRM nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-171">The client application obtains BMC data through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-172">**Interfaccia di gestione piattaforma intelligente (IPMI)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-172">**Intelligent Platform Management Interface (IPMI)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-173">Standard del settore IT per l'architettura di [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-173">An IT industry standard for the architecture of [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-174">Le funzionalità di gestione hardware di Windows forniscono un [*driver IPMI*](windows-remote-management-glossary.md) e un [*provider IPMI*](windows-remote-management-glossary.md) WMI che consentono di ottenere dati BMC tramite script di gestione, strumenti da riga di comando e applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-174">The Windows hardware management features supply an [*IPMI driver*](windows-remote-management-glossary.md) and a WMI [*IPMI provider*](windows-remote-management-glossary.md) that allow management scripts, command-line tools, and applications to obtain BMC data.</span></span> <span data-ttu-id="fc4d6-175">Il provider IPMI dispone di [classi](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-175">The IPMI provider has WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-176">**IPMI**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-176">**IPMI**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-177">Vedere [*Intelligent Platform Management Interface (impi)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-177">See [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-178">**Driver IPMI**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-178">**IPMI driver**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-179">Driver del kernel che consente di accedere ai dispositivi [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) dai componenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-179">The kernel driver that enables access to [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) devices from the operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-180">**Provider IPMI**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-180">**IPMI provider**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-181">Provider WMI standard che definisce le classi che modellano l' [*IPMI*](windows-remote-management-glossary.md) e i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-181">A standard WMI provider that defines classes modeling the [*IPMI*](windows-remote-management-glossary.md) and its data.</span></span> <span data-ttu-id="fc4d6-182">Il [provider IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) è una DLL COM che ottiene i dati dal BMC.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-182">The [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) is a COM DLL that obtains data from the BMC.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="fc4d6-183">K</span><span class="sxs-lookup"><span data-stu-id="fc4d6-183">K</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-184">**KCS**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-184">**KCS**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-185">Vedere [*stile del controller della tastiera (KCS)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-185">See [*Keyboard Controller Style (KCS)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-186">**Autenticazione Kerberos**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-186">**Kerberos authentication**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-187">Metodo di autenticazione reciproca tra il client e il server che utilizza chiavi crittografate.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-187">A method of mutual authentication between the client and server that uses encrypted keys.</span></span> <span data-ttu-id="fc4d6-188">Per i computer in cui è in esecuzione un sistema operativo basato su Windows, l'account client deve essere un account di dominio nello stesso dominio del server.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-188">For computers running on a Windows-based operating system, the client account must be a domain account in the same domain as the server.</span></span> <span data-ttu-id="fc4d6-189">Quando un client utilizza credenziali predefinite, Kerberos è il metodo di autenticazione se la stringa di connessione non è una delle seguenti: localhost, 127.0.0.1 o \[ :: 1 \] .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-189">When a client uses default credentials, Kerberos is the authentication method if the connection string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-190">**Stile del controller della tastiera (KCS)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-190">**Keyboard Controller Style (KCS)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-191">Il protocollo usato dal [*driver IPMI*](windows-remote-management-glossary.md) per comunicare con il [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-191">The protocol used by the [*IPMI driver*](windows-remote-management-glossary.md) to communicate with the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="fc4d6-192">L</span><span class="sxs-lookup"><span data-stu-id="fc4d6-192">L</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-193">**listener**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-193">**listener**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-194">Un servizio di gestione che implementa WS-Management protocollo per inviare e ricevere messaggi.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-194">A management service that implements WS-Management protocol to send and receive messages.</span></span> <span data-ttu-id="fc4d6-195">WinRM è un servizio di listener.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-195">WinRM is a listener service.</span></span> <span data-ttu-id="fc4d6-196">Un listener viene definito da un trasporto (HTTP o HTTPS) e da un indirizzo IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-196">A listener is defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span> <span data-ttu-id="fc4d6-197">È possibile creare più di un'istanza del listener WinRM in un singolo computer assegnando loro un indirizzo TCP/IP o un numero di porta diverso.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-197">You can create more than one WinRM listener instance on a single computer by giving them a different TCP/IP address or port number.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="fc4d6-198">M</span><span class="sxs-lookup"><span data-stu-id="fc4d6-198">M</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-199">**message**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-199">**message**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-200">Un pacchetto di informazioni trasmesse tra computer o reti separate costruite con il protocollo [*SOAP*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-200">A package of information transmitted between computers or separate networks constructed with the [*SOAP*](windows-remote-management-glossary.md) protocol.</span></span> <span data-ttu-id="fc4d6-201">Nel pacchetto è presente un'intestazione che descrive la destinazione e il trasporto del messaggio e un corpo che contiene il contenuto da utilizzare all'arrivo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-201">The package has a header, that describes the message target and transport, and a body that contains the content to be used when the message arrives.</span></span> <span data-ttu-id="fc4d6-202">Un messaggio è costituito da una combinazione di elementi di specifiche quali [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-202">A message is a combination of elements from specifications such as [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="fc4d6-203">N</span><span class="sxs-lookup"><span data-stu-id="fc4d6-203">N</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-204">**namespace**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-204">**namespace**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-205">Uno spazio dei nomi [*WMI*](windows-remote-management-glossary.md) , ovvero un raggruppamento logico di classi e istanze WMI per controllare l'ambito e l'accesso.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-205">A [*WMI*](windows-remote-management-glossary.md) namespace, which is a logical grouping of WMI classes and instances to control scope and access.</span></span> <span data-ttu-id="fc4d6-206">L'origine dei dati di gestione più frequente per i sistemi che eseguono Windows è lo \\ spazio dei nomi CIMV2 radice, che contiene classi come il [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-206">The most frequent source of management data for systems running Windows is the root\\cimv2 namespace, which contains classes such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="fc4d6-207">Gli spazi dei nomi vengono visualizzati nell'URI della risorsa per le classi WMI, ad esempio https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-207">Namespaces appear in the resource URI for WMI classes, for example https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-208">**Negozia autenticazione**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-208">**Negotiate authentication**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-209">Tipo di autenticazione negoziato e Single Sign-on che rappresenta l'implementazione di Windows del [*meccanismo di negoziazione GSSAPI semplice e protetto (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-209">A negotiated, single sign on type of authentication that is the Windows implementation of [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-210">La negoziazione SPNEGO determina se l'autenticazione è gestita da Kerberos o NTLM.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-210">SPNEGO negotiation determines whether authentication is handled by Kerberos or NTLM.</span></span> <span data-ttu-id="fc4d6-211">Kerberos è il meccanismo preferito.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-211">Kerberos is the preferred mechanism.</span></span> <span data-ttu-id="fc4d6-212">L'autenticazione Negotiate nei sistemi basati su Windows è detta anche autenticazione integrata di Windows.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-212">Negotiate authentication on Windows-based systems is also called Windows Integrated Authentication.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-213">**sensore numerico**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-213">**numeric sensor**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-214">Tipo numerico di sensore in un [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md), ad esempio temperatura o tensione.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-214">A numeric type of sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md), for example temperature or voltage.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="fc4d6-215">O</span><span class="sxs-lookup"><span data-stu-id="fc4d6-215">O</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-216">**opzione**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-216">**option**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-217">Dati aggiuntivi richiesti dal provider di risorse per elaborare una richiesta.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-217">The additional data required by the resource provider to process a request.</span></span> <span data-ttu-id="fc4d6-218">Alcuni provider WMI, ad esempio, richiedono dati aggiuntivi forniti come oggetti [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-218">For example, some WMI providers require additional data supplied as [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) objects.</span></span> <span data-ttu-id="fc4d6-219">Il supporto dell'opzione è disponibile nell'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-219">Option support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-220">**fuori banda**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-220">**out-of-band**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-221">L'applicazione client ottiene i dati direttamente dal [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) di un altro computer, anziché tramite il [*listener*](windows-remote-management-glossary.md) WinRM nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-221">The client application obtains data directly from the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) of another computer, rather than through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="fc4d6-222">P</span><span class="sxs-lookup"><span data-stu-id="fc4d6-222">P</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-223">**tirare**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-223">**pull**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-224">Viene inviato un messaggio pull [*WS-Enumeration*](windows-remote-management-glossary.md) per continuare un'enumerazione avviata da una chiamata iniziale a WS-Enumeration: enumerate.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-224">A [*WS-Enumeration*](windows-remote-management-glossary.md) pull message is sent to continue an enumeration started by an initial call to WS-Enumeration:Enumerate.</span></span> <span data-ttu-id="fc4d6-225">L'operazione pull nel servizio gestione remota Windows viene eseguita da [**Enumerator. ReadItem**](enumerator-readitem.md) o [**IWSManEnumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-225">The pull operation in the WinRM service is performed by [**Enumerator.ReadItem**](enumerator-readitem.md) or [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="fc4d6-226">R</span><span class="sxs-lookup"><span data-stu-id="fc4d6-226">R</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-227">**risorse**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-227">**resource**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-228">[*Endpoint*](windows-remote-management-glossary.md) che rappresenta un tipo distinto di operazione di gestione o valore.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-228">An [*endpoint*](windows-remote-management-glossary.md) that represents a distinct type of management operation or value.</span></span> <span data-ttu-id="fc4d6-229">Un servizio espone una o più risorse e alcune risorse possono avere più di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-229">A service exposes one or more resources and some resources can have more than one instance.</span></span> <span data-ttu-id="fc4d6-230">Una risorsa di gestione è simile a una classe WMI o a una tabella di database e un'istanza è simile a un'istanza della classe o a una riga nella tabella.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-230">A management resource is similar to a WMI class or a database table, and an instance is similar to an instance of the class or a row in the table.</span></span> <span data-ttu-id="fc4d6-231">Ad esempio, la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) rappresenta una risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-231">For example, the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class represents a resource.</span></span> <span data-ttu-id="fc4d6-232">`Win32_LogicalDisk="C:\"` è un'istanza specifica della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-232">`Win32_LogicalDisk="C:\"` is a specific instance of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-233">**URI risorsa**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-233">**resource URI**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-234">[*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) usato per identificare un tipo specifico di risorsa, ad esempio i dischi o i processi, in un sistema.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-234">The [*uniform resource identifier (URI)*](windows-remote-management-glossary.md) used to identify a specific type of resource, such as disks or processes, on a system.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="fc4d6-235">S</span><span class="sxs-lookup"><span data-stu-id="fc4d6-235">S</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-236">**SEL**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-236">**SEL**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-237">Vedere [*registro eventi di sistema (SEL)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-237">See [*System Event Log (SEL)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-238">**Adapter SEL**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-238">**SEL adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-239">Adapter che invia i dati di [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) all' [*agente di raccolta eventi*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-239">The adapter that sends [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) data to the [*Event Collector*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-240">**selector**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-240">**selector**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-241">Coppia di nome e valore che rappresenta una particolare istanza di una [*risorsa*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-241">A name and value pair that represents a particular instance of a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-242">Si tratta essenzialmente di un filtro o di una "chiave" che identifica l'istanza desiderata della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-242">This is essentially a filter or "key" that identifies the desired instance of the resource.</span></span> <span data-ttu-id="fc4d6-243">Il supporto del selettore si trova nell'oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-243">Selector support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-244">**sensore**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-244">**sensor**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-245">Un dispositivo di misurazione in un [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-245">A measurement device in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-246">**servizio**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-246">**service**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-247">Applicazione che fornisce servizi di gestione ai client tramite il protocollo WS-Management e altri [*servizi Web*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-247">An application that provides management services to clients through the WS-Management protocol and other [*web services*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-248">Un servizio è in genere lo stesso del [*listener*](windows-remote-management-glossary.md) in una rete.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-248">A service is usually the same as the [*listener*](windows-remote-management-glossary.md) on a network.</span></span> <span data-ttu-id="fc4d6-249">Il servizio dispone di un indirizzo di trasporto fisico.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-249">The service has a physical transport address.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-250">**sessione**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-250">**session**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-251">Connessione tra un [*client*](windows-remote-management-glossary.md) gestione remota Windows e il [*listener*](windows-remote-management-glossary.md)WinRM locale o remoto oppure il servizio.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-251">A connection between a Windows Remote Management [*client*](windows-remote-management-glossary.md) and the local or remote WinRM [*listener*](windows-remote-management-glossary.md), or service.</span></span> <span data-ttu-id="fc4d6-252">Questa connessione è simile alla connessione tra uno script client WMI e WMI in un server remoto.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-252">This connection is similar to the connection between a WMI client script and WMI on a remote server.</span></span> <span data-ttu-id="fc4d6-253">Le operazioni di sessione, ad esempio l'enumerazione di una risorsa (enumerazione), il recupero di un'istanza di una risorsa (Get) o l'esecuzione di un metodo di risorsa (Invoke) sono metodi dell'oggetto **Session** .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-253">The session operations, such as enumerating a resource (Enumerate), getting an instance of a resource (Get), or running a resource method (Invoke) are methods of the **Session** object.</span></span> <span data-ttu-id="fc4d6-254">Un oggetto **sessione** viene creato da [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-254">A **Session** object is created by [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-255">**Simple and Protected GSS-meccanismo di negoziazione API (SPNEGO)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-255">**Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-256">Meccanismo di autenticazione utilizzato dal client o dal server che riceve le richieste di dati tramite WinRM in un contesto di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-256">An authentication mechanism used by the client or server receiving requests for data through the WinRM in an Active Directory context.</span></span> <span data-ttu-id="fc4d6-257">SPNEGO si basa su un protocollo RFC (Request for Comments) prodotto da Internet Engineering Task Force (IETF).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-257">SPNEGO is based on an Request For Comments (RFC) protocol produced by the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="fc4d6-258">SPNEGO è anche noto come [*autenticazione integrata di Windows*](windows-remote-management-glossary.md), il termine usato negli argomenti della guida Gestione remota Windows.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-258">SPNEGO is also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md), the term used in the Windows Remote Management help topics.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-259">**Simple Object Access Protocol (SOAP)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-259">**Simple Object Access Protocol (SOAP)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-260">Protocollo basato su XML utilizzato dai servizi Web.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-260">An XML-based protocol used by web services.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-261">**SOAP**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-261">**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-262">Vedere [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-262">See [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-263">**SPNEGO**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-263">**SPNEGO**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-264">Vedere la pagina relativa al [*meccanismo di negoziazione API (SPNEGO) semplice e protetto*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-264">See [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-265">**Registro eventi di sistema (SEL)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-265">**System Event Log (SEL)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-266">Database di eventi nell'hardware [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-266">The database of events in the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) hardware.</span></span> <span data-ttu-id="fc4d6-267">L' [*Adapter SEL*](windows-remote-management-glossary.md) trasmette questi eventi al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-267">The [*SEL adapter*](windows-remote-management-glossary.md) conveys these events to the operating system.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="fc4d6-268">U</span><span class="sxs-lookup"><span data-stu-id="fc4d6-268">U</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-269">**Uniform Resource Identifier (URI)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-269">**uniform resource identifier (URI)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-270">Stringa che identifica una risorsa nell'azienda, ad esempio un computer, un processo, un'unità disco o un sensore di temperatura in un [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-270">A string that identifies a resource in the enterprise, such as a computer, a process, a disk drive, or a temperature sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-271">L'URI è il meccanismo di indirizzamento dei servizi Web definito in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): sintassi generica \[ RFC3986 \] .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-271">The URI is the web service addressing mechanism defined in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Generic Syntax \[RFC3986\].</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-272">**URI**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-272">**URI**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-273">Vedere [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-273">See [*uniform resource identifier (URI)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="fc4d6-274">W</span><span class="sxs-lookup"><span data-stu-id="fc4d6-274">W</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-275">**servizio Web**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-275">**web service**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-276">Applicazione software utilizzata per l'interazione tra computer in Internet o in una rete.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-276">A software application used for interaction between computers across the Internet or a network.</span></span> <span data-ttu-id="fc4d6-277">I servizi Web sono descritti da [*WSDL (Web Service Description Language)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-277">Web services are described by the [*Web Service Description Language (WSDL)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-278">La descrizione specifica del servizio Web indica ad altri servizi come interagire con il servizio Web utilizzando messaggi SOAP.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-278">The specific description of the web service tells other services how to interact with the web service by using SOAP messages.</span></span> <span data-ttu-id="fc4d6-279">I messaggi vengono trasmessi tra computer da un trasporto, in genere HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-279">The messages are conveyed between computers by a transport, typically HTTP or HTTPS.</span></span> <span data-ttu-id="fc4d6-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)e [*WS-Management*](windows-remote-management-glossary.md) sono esempi di protocolli utilizzati dalle applicazioni del servizio Web per comunicare tra loro.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md) are examples of protocols used by web service applications to communicate with each other.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-281">**WSDL (Web Service Description Language)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-281">**Web Service Description Language (WSDL)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-282">Linguaggio basato su XML utilizzato per definire la modalità di interazione con un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-282">An XML-based language used to define how to interact with a web service.</span></span> <span data-ttu-id="fc4d6-283">In genere, WSDL descrive i messaggi SOAP richiesti dal servizio Web per restituire i dati o eseguire operazioni.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-283">Typically, the WSDL describes what SOAP messages the web service requires to return data or carry out operations.</span></span> <span data-ttu-id="fc4d6-284">WSDL consente a un'implementazione di un sistema operativo di comunicare con il servizio Web implementato in un altro sistema operativo, purché siano soddisfatti i requisiti del documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-284">The WSDL allows an implementation from one operating system to communicate with the web service implemented on another operating system, as long as the requirements of the WSDL are met.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-285">**Autenticazione integrata di Windows**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-285">**Windows Integrated Authentication**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-286">Vedere [*Negotiate Authentication*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-286">See [*Negotiate authentication*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-287">**Strumentazione gestione Windows (WMI)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-287">**Windows Management Instrumentation (WMI)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-288">Implementazione Microsoft dello standard WBEM (Web-Based Enterprise Management) pubblicata da [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-288">The Microsoft implementation of the Web-Based Enterprise Management (WBEM) standard published by the [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="fc4d6-289">WMI consente di gestire computer locali e remoti e di modellare oggetti computer e di rete utilizzando un'estensione dello standard [*Common Information Model (CIM)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="fc4d6-289">WMI allows you to manage local and remote computers and models computer and network objects using an extension of the [*Common Information Model (CIM)*](windows-remote-management-glossary.md) standard.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-290">**Gestione remota Windows (WinRM)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-290">**Windows Remote Management (WinRM)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-291">Implementazione Microsoft di un servizio Web di gestione basato sul protocollo [*WS-Management*](windows-remote-management-glossary.md) pubblico standard.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-291">The Microsoft implementation of a management web service based on the public standard [*WS-Management*](windows-remote-management-glossary.md) protocol.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-292">**Shell remota Windows (WinRS)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-292">**Windows Remote Shell (WinRS)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-293">Uno strumento della shell che si basa su [*gestione remota Windows*](windows-remote-management-glossary.md) per eseguire comandi remoti, specialmente per i server Head.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-293">A shell tool that relies on [*Windows Remote Management*](windows-remote-management-glossary.md) to execute remote commands, especially for headless servers.</span></span> <span data-ttu-id="fc4d6-294">Lo strumento da riga di comando è Winrs.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-294">The command-line tool is Winrs.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-295">**WMI**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-295">**WMI**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-296">Vedere [*Strumentazione gestione Windows (WMI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-296">See [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-297">**Plug-in WMI**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-297">**WMI plug-in**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-298">Il plug-in WinRM che rende disponibili i dati WMI ai client WinRM.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-298">The WinRM plug-in that makes WMI data available to WinRM clients.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-299">**WS-Addressing (WSA)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-299">**WS-Addressing (wsa)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-300">Protocollo standard pubblico, che è basato su SOAP, che consente di creare un sistema di indirizzamento utilizzato nelle intestazioni dei messaggi inviati attraverso Internet.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-300">A public standard protocol, which is SOAP-based, that creates an addressing system used in the headers of messages sent across the Internet.</span></span> <span data-ttu-id="fc4d6-301">Lo standard definisce il modo in cui le risorse possono essere posizionate tra le reti e i firewall.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-301">The standard defines how resources can be located across networks and firewalls.</span></span> <span data-ttu-id="fc4d6-302">WS-Addressing è uno dei protocolli del servizio Web che compongono il protocollo di WS-Management.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-302">WS-Addressing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-303">**WS-Enumeration (wsen)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-303">**WS-Enumeration (wsen)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-304">Protocollo standard pubblico, che è basato su SOAP, per l'enumerazione di una sequenza di elementi XML che possono rappresentare raccolte di dati, log o altre strutture di informazioni lineari.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-304">A public standard protocol, which is SOAP-based, for enumerating a sequence of XML elements that may represent data collections, logs, or other linear information structures.</span></span> <span data-ttu-id="fc4d6-305">WS-Enumeration è uno dei protocolli del servizio Web che compongono il protocollo di WS-Management.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-305">WS-Enumeration is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-306">**WS-Eventing (WSE)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-306">**WS-Eventing (wse)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-307">Protocollo standard pubblico, che è basato su SOAP, che consente a un servizio Web (Sottoscrittore) di sottoscrivere e accettare messaggi di notifica degli eventi da un altro servizio Web (origine evento).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-307">A public standard protocol, which is SOAP-based, that allows one web service (the subscriber) to subscribe to and accept event notification messages from another web service (the event source).</span></span> <span data-ttu-id="fc4d6-308">WS-Eventing è uno dei protocolli del servizio Web che compongono il protocollo di WS-Management.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-308">WS-Eventing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-309">**WS-Management**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-309">**WS-Management**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-310">Protocollo standard pubblico, che è basato su SOAP, per la condivisione di dati di gestione tra tutti i sistemi operativi, i computer e i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-310">A public standard protocol, which is SOAP-based, for sharing management data among all operating systems, computers, and devices.</span></span> <span data-ttu-id="fc4d6-311">Tutti [*i messaggi*](windows-remote-management-glossary.md) inviati dal client o dai componenti del server WinRM utilizzano questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-311">All [*messages*](windows-remote-management-glossary.md) sent by the WinRM client or server components use this protocol.</span></span>

</dd> <dt>

<span data-ttu-id="fc4d6-312">**WS-Transfer (wxf)**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-312">**WS-Transfer (wxf)**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-313">Protocollo standard pubblico, che è basato su SOAP, per l'accesso alle rappresentazioni XML di risorse basate su servizi Web tramite un semplice set di verbi come Get, put, Invoke o DELETE.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-313">A public standard protocol, which is SOAP-based, for accessing XML representations of web service-based resources through a simple set of verbs such as Get, Put, Invoke, or Delete.</span></span> <span data-ttu-id="fc4d6-314">WS-Transfer definisce le operazioni per l'invio e la ricezione della rappresentazione di una determinata risorsa e operazioni per la creazione o l'eliminazione di una risorsa e la relativa rappresentazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-314">WS-Transfer defines operations for sending and receiving the representation of a particular resource and operations for creating or deleting a resource and its corresponding representation.</span></span>

</dd> </dl>

## <a name="x"></a><span data-ttu-id="fc4d6-315">X</span><span class="sxs-lookup"><span data-stu-id="fc4d6-315">X</span></span>

<dl> <dt>

<span data-ttu-id="fc4d6-316">**XPath**</span><span class="sxs-lookup"><span data-stu-id="fc4d6-316">**XPath**</span></span>
</dt> <dd>

<span data-ttu-id="fc4d6-317">Notazione di percorso per l'indirizzamento di parti di un documento XML, in modo analogo a un URL.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-317">A path notation for addressing parts of an XML document, similar to a URL.</span></span> <span data-ttu-id="fc4d6-318">Un'espressione XPath è una sequenza di frasi da ottenere dalla posizione corrente nel documento XML a un altro nodo o a un set di nodi.</span><span class="sxs-lookup"><span data-stu-id="fc4d6-318">An XPath expression is a sequence of phrases to get from the current location in the XML document to another node or set of nodes.</span></span> <span data-ttu-id="fc4d6-319">Le frasi sono separate da caratteri di barra ("/").</span><span class="sxs-lookup"><span data-stu-id="fc4d6-319">The phrases are separated by forward-slash ("/") characters.</span></span> <span data-ttu-id="fc4d6-320">Il servizio WinRM supporta [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) per il [*dialetto del frammento*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="fc4d6-320">The WinRM service supports [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) for [*fragment dialect*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

 

 