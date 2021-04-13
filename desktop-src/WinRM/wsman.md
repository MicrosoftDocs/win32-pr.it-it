---
title: Oggetto WSMan (WSManDisp. h)
description: Fornisce metodi e proprietà utilizzati per creare una sessione, rappresentata da un oggetto sessione.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto WSMan
- Gestione remota Windows oggetto WSMan, descritto
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400296"
---
# <a name="wsman-object"></a><span data-ttu-id="b9c58-105">WSMan (oggetto)</span><span class="sxs-lookup"><span data-stu-id="b9c58-105">WSMan object</span></span>

<span data-ttu-id="b9c58-106">Fornisce metodi e proprietà utilizzati per creare una sessione, rappresentata da un oggetto [**sessione**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c58-106">Provides methods and properties used to create a session, represented by a [**Session**](session.md) object.</span></span> <span data-ttu-id="b9c58-107">Qualsiasi operazione di Gestione remota Windows richiede la creazione di una [**sessione**](session.md) che si connette a un computer remoto, a un [*controller di gestione di base*](windows-remote-management-glossary.md) (BMC) o al computer locale.</span><span class="sxs-lookup"><span data-stu-id="b9c58-107">Any Windows Remote Management operations require creation of a [**Session**](session.md) that connects to a remote computer, [*base management controller*](windows-remote-management-glossary.md) (BMC), or the local computer.</span></span> <span data-ttu-id="b9c58-108">Le operazioni includono il recupero, la scrittura, l'enumerazione dei dati o la chiamata di metodi.</span><span class="sxs-lookup"><span data-stu-id="b9c58-108">Operations include getting, writing, enumerating data, or invoking methods.</span></span>

## <a name="members"></a><span data-ttu-id="b9c58-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b9c58-109">Members</span></span>

<span data-ttu-id="b9c58-110">L'oggetto **WSMan** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b9c58-110">The **WSMan** object has these types of members:</span></span>

-   [<span data-ttu-id="b9c58-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="b9c58-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b9c58-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9c58-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b9c58-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="b9c58-113">Methods</span></span>

<span data-ttu-id="b9c58-114">Questi metodi sono disponibili nell'oggetto **WSMan** .</span><span class="sxs-lookup"><span data-stu-id="b9c58-114">The **WSMan** object has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b9c58-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="b9c58-115">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b9c58-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9c58-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-117"><a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-118">Crea un oggetto <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> che specifica il nome utente e la password utilizzati durante la creazione di una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="b9c58-118">Creates a <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> object that specifies the user name and password used when creating a remote session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-119"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-120">Crea un oggetto <a href="resourcelocator.md"><strong>resourceLocator</strong></a> che può specificare:</span><span class="sxs-lookup"><span data-stu-id="b9c58-120">Creates a <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> object that can specify:</span></span><br/>
<ul>
<li><span data-ttu-id="b9c58-121">Percorso completo di una <a href="windows-remote-management-glossary.md"><em>risorsa</em></a> o di un singolo elemento di dati.</span><span class="sxs-lookup"><span data-stu-id="b9c58-121">The complete path to a <a href="windows-remote-management-glossary.md"><em>resource</em></a> or a single piece of data.</span></span></li>
<li><span data-ttu-id="b9c58-122"><a href="windows-remote-management-glossary.md"><em>Selettore</em></a> per un'istanza specifica di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="b9c58-122">A <a href="windows-remote-management-glossary.md"><em>selector</em></a> for a specific instance of a resource.</span></span></li>
<li><span data-ttu-id="b9c58-123"><a href="windows-remote-management-glossary.md"><em>Opzione</em></a> che fornisce dati aggiuntivi al provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9c58-123">An <a href="windows-remote-management-glossary.md"><em>option</em></a> that supplies additional data to the resource provider.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-124"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-125">Crea un oggetto <a href="session.md"><strong>sessione</strong></a> che può quindi essere utilizzato per le operazioni di rete successive.</span><span class="sxs-lookup"><span data-stu-id="b9c58-125">Creates a <a href="session.md"><strong>Session</strong></a> object that can then be used for subsequent network operations.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-126"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-127">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyDeep</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-127">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeep</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-128"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-129">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-129">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-130"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-131">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagHierarchyShallow</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-131">Returns the value of the enumeration flag <strong>EnumerationFlagHierarchyShallow</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-132"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-133">Restituisce il valore della costante di enumerazione <strong>WSManFlagNonXmlText</strong> per l'utilizzo nel parametro <em>Flags</em> del metodo <a href="session-enumerate.md"><strong>Session. enumerate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b9c58-133">Returns the value of the enumeration constant <strong>WSManFlagNonXmlText</strong> for use in the <em>flags</em> parameter of the <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a> method.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-134"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-135">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnEPR</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-135">Returns the value of the enumeration flag <strong>EnumerationFlagReturnEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-136"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-137">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnObject</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-137">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObject</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-138"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-139">Restituisce il valore del flag di enumerazione <strong>EnumerationFlagReturnObjectAndEPR</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="session-enumerate.md"><strong>Session. enumerate</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-139">Returns the value of the enumeration flag <strong>EnumerationFlagReturnObjectAndEPR</strong> for use in the <em>flags</em> parameter of <a href="session-enumerate.md"><strong>Session.Enumerate</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-140"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-140"><a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-141">Restituisce una stringa formattata contenente il testo di un numero di errore.</span><span class="sxs-lookup"><span data-stu-id="b9c58-141">Returns a formatted string containing the text of an error number.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-142"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-143">Restituisce il valore del flag di autenticazione <strong>WSManFlagCredUsernamePassword</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-143">Returns the value of the authentication flag <strong>WSManFlagCredUsernamePassword</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-144"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-145">Restituisce il valore del flag di autenticazione <strong>WSManFlagEnableSPNServerPort</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-145">Returns the value of the authentication flag <strong>WSManFlagEnableSPNServerPort</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-146"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-147">Restituisce il valore del flag di autenticazione <strong>WSManFlagNoEncryption</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-147">Returns the value of the authentication flag <strong>WSManFlagNoEncryption</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-148"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-149">Restituisce il valore del flag di autenticazione <strong>WSManFlagSkipCACheck</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-149">Returns the value of the <strong>WSManFlagSkipCACheck</strong> authentication flag for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-150"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-151">Restituisce il valore del flag di autenticazione <strong>WSManFlagSkipCNCheck</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-151">Returns the value of the authentication flag <strong>WSManFlagSkipCNCheck</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-152"><a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-153">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseBasic</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-153">Returns the value of the authentication flag <strong>WSManFlagUseBasic</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-154"><a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-155">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseDigest</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-155">Returns the value of the authentication flag <strong>WSManFlagUseDigest</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-156"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-157">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseKerberos</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-157">Returns the value of the authentication flag <strong>WSManFlagUseKerberos</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-158"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-159">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseNegotiate</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-159">Returns the value of the authentication flag <strong>WSManFlagUseNegotiate</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="b9c58-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-160"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-161">Restituisce il valore del flag di autenticazione <strong>WSManFlagUseNoAuthentication</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-161">Returns the value of the authentication flag <strong>WSManFlagUseNoAuthentication</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="b9c58-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></span><span class="sxs-lookup"><span data-stu-id="b9c58-162"><a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="b9c58-163">Restituisce il valore del flag di autenticazione <strong>WSManFlagUTF8</strong> per l'utilizzo nel parametro <em>Flags</em> di <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b9c58-163">Returns the value of the authentication flag <strong>WSManFlagUTF8</strong> for use in the <em>flags</em> parameter of <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="b9c58-164">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9c58-164">Properties</span></span>

<span data-ttu-id="b9c58-165">L'oggetto **WSMan** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b9c58-165">The **WSMan** object has these properties.</span></span>



| <span data-ttu-id="b9c58-166">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b9c58-166">Property</span></span>                                            | <span data-ttu-id="b9c58-167">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b9c58-167">Access type</span></span>          | <span data-ttu-id="b9c58-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9c58-168">Description</span></span>                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="b9c58-169">**CommandLine**</span><span class="sxs-lookup"><span data-stu-id="b9c58-169">**CommandLine**</span></span>](wsman-commandline.md)<br/> | <span data-ttu-id="b9c58-170">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b9c58-170">Read-only</span></span><br/> | <span data-ttu-id="b9c58-171">Ottiene la riga di comando non elaborata per il processo di hosting corrente.</span><span class="sxs-lookup"><span data-stu-id="b9c58-171">Gets the unprocessed command line for the current hosting process.</span></span><br/> |
| [<span data-ttu-id="b9c58-172">**Errore**</span><span class="sxs-lookup"><span data-stu-id="b9c58-172">**Error**</span></span>](wsman-error.md)<br/>             | <span data-ttu-id="b9c58-173">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b9c58-173">Read-only</span></span><br/> | <span data-ttu-id="b9c58-174">Ottiene le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="b9c58-174">Gets error information.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="b9c58-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9c58-175">Remarks</span></span>

<span data-ttu-id="b9c58-176">L'oggetto **WSMan** corrisponde alle interfacce [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) .</span><span class="sxs-lookup"><span data-stu-id="b9c58-176">The **WSMan** object corresponds to the [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) interfaces.</span></span> <span data-ttu-id="b9c58-177">**WSMan** è l'unico oggetto che può essere creato direttamente usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9c58-177">**WSMan** is the only object that can be created directly using [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="b9c58-178">Esempio</span><span class="sxs-lookup"><span data-stu-id="b9c58-178">Examples</span></span>

<span data-ttu-id="b9c58-179">Nell'esempio di codice seguente viene illustrato come creare un'istanza di un oggetto **WSMan** .</span><span class="sxs-lookup"><span data-stu-id="b9c58-179">The following code example shows how to instantiate a **WSMan** object.</span></span>


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a><span data-ttu-id="b9c58-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9c58-180">Requirements</span></span>



| <span data-ttu-id="b9c58-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c58-181">Requirement</span></span> | <span data-ttu-id="b9c58-182">Valore</span><span class="sxs-lookup"><span data-stu-id="b9c58-182">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c58-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c58-183">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c58-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9c58-184">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b9c58-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c58-185">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c58-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9c58-186">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b9c58-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9c58-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9c58-188"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c58-188"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9c58-189">IDL</span><span class="sxs-lookup"><span data-stu-id="b9c58-189">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9c58-190"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9c58-190"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9c58-191">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9c58-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9c58-192"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b9c58-192"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b9c58-193">DLL</span><span class="sxs-lookup"><span data-stu-id="b9c58-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9c58-194"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c58-194"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b9c58-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9c58-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c58-196">API di scripting WinRM</span><span class="sxs-lookup"><span data-stu-id="b9c58-196">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="b9c58-197">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="b9c58-197">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b9c58-198">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="b9c58-198">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b9c58-199">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="b9c58-199">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b9c58-200">Recupero di dati dal computer locale</span><span class="sxs-lookup"><span data-stu-id="b9c58-200">Obtaining Data from the Local Computer</span></span>](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[<span data-ttu-id="b9c58-201">Recupero di dati da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="b9c58-201">Obtaining Data from a Remote Computer</span></span>](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

