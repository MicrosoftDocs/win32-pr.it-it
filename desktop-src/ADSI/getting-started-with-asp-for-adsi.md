---
title: Introduzione con ASP per ADSI
description: È possibile utilizzare ADSI per accedere ai dati della directory utilizzando una pagina ASP. Si tratta di un modo pratico per eseguire le attività di amministrazione e le query da una pagina Web o fornire informazioni ai dipendenti in una rete Intranet.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ASP ADSI
- ADSI, pagine ASP
- ADSI, ASP Pages, esempio di codice ASP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707420"
---
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="51205-107">Introduzione con ASP per ADSI</span><span class="sxs-lookup"><span data-stu-id="51205-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="51205-108">È possibile utilizzare ADSI per accedere ai dati della directory utilizzando una pagina ASP.</span><span class="sxs-lookup"><span data-stu-id="51205-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="51205-109">Si tratta di un modo pratico per eseguire le attività di amministrazione e le query da una pagina Web o fornire informazioni ai dipendenti in una rete Intranet.</span><span class="sxs-lookup"><span data-stu-id="51205-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="51205-110">Uno dei vantaggi dell'utilizzo di ADSI con ASP è la possibilità di creare un'esperienza utente più completa, in quanto è possibile utilizzare Visual Basic per creare un'applicazione ADSI e offrirla a un utente tramite una pagina Web standard.</span><span class="sxs-lookup"><span data-stu-id="51205-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="51205-111">Ad esempio, è possibile creare una pagina Web che consente ai dipendenti di immettere il cognome di un dipendente e ottenere un numero di telefono per quel dipendente oppure creare un modulo che consenta ai dipendenti di aggiornare le informazioni personali in un database delle risorse umane della società.</span><span class="sxs-lookup"><span data-stu-id="51205-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="51205-112">Il codice ASP inizia con "<%" e termina con "% >".</span><span class="sxs-lookup"><span data-stu-id="51205-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="51205-113">È possibile aggiungere il codice ADSI come VBScript o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="51205-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="51205-114">Per creare una pagina ASP, è possibile usare un editor di pagine Web, un blocco note o un altro editor di testo o il sistema di sviluppo Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="51205-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="51205-115">Prima di eseguire la pagina ASP, configurare l'applicazione o il server IIS seguendo le istruzioni disponibili in [problemi di autenticazione per ADSI con ASP](authentication-issues-for-adsi-with-asp.md).</span><span class="sxs-lookup"><span data-stu-id="51205-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="51205-116">Esempio ASP semplice: enumerazione di oggetti in un contenitore</span><span class="sxs-lookup"><span data-stu-id="51205-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="51205-117">Usando un editor di pagine Web, creare una nuova pagina HTML che accetti il nome distinto di un oggetto contenitore.</span><span class="sxs-lookup"><span data-stu-id="51205-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="51205-118">Immettere l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="51205-118">Enter the following code example.</span></span>


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



<span data-ttu-id="51205-119">In questa pagina è ora possibile accettare un nome di contenitore che viene passato e utilizzare ADSI per enumerare gli oggetti nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="51205-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="51205-120">Creare una nuova pagina ASP denominata Enum. asp e immettere l'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="51205-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="51205-121">Salvare questa pagina nella radice del server Web locale.</span><span class="sxs-lookup"><span data-stu-id="51205-121">Save this page at the root of the local web server.</span></span>


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




