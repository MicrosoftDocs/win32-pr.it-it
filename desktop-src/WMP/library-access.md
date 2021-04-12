---
title: Accesso alla libreria
description: Accesso alla libreria
ms.assetid: 9f722531-a551-4ca9-be5f-01a291a180b0
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Windows Media Player Library, accesso
- libreria, accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb1a8fcc34324775d968f6eab49003c28452f76c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329876"
---
# <a name="library-access"></a><span data-ttu-id="94604-112">Accesso alla libreria</span><span class="sxs-lookup"><span data-stu-id="94604-112">Library Access</span></span>

<span data-ttu-id="94604-113">Le proprietà e i metodi del modello a oggetti di Windows Media Player che accedono alla libreria richiedono l'accesso in sola lettura o in lettura/scrittura al database.</span><span class="sxs-lookup"><span data-stu-id="94604-113">Properties and methods of the Windows Media Player object model that access the library require either read-only or read/write access to the database.</span></span> <span data-ttu-id="94604-114">La libreria contiene informazioni che alcuni utenti vogliono tenere privato e che devono essere accessibili o modificate solo con il loro consenso.</span><span class="sxs-lookup"><span data-stu-id="94604-114">The library contains information that some users want to keep private and that should be accessed or altered only with their consent.</span></span>

<span data-ttu-id="94604-115">Per Windows Media Player 9 Series o versioni successive, è possibile determinare il livello di accesso a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="94604-115">For Windows Media Player 9 Series or later, you can programmatically determine access level.</span></span> <span data-ttu-id="94604-116">Per determinare il livello corrente di accesso concesso al codice, recuperare le *Impostazioni*. proprietà **mediaAccessRights** .</span><span class="sxs-lookup"><span data-stu-id="94604-116">To determine the current level of access granted to your code, retrieve the *Settings*.**mediaAccessRights** property.</span></span> <span data-ttu-id="94604-117">Tale proprietà restituisce "None", "Read" o "full" (Read/Write).</span><span class="sxs-lookup"><span data-stu-id="94604-117">That property returns "none", "read", or "full" (read/write).</span></span> <span data-ttu-id="94604-118">Per richiedere diritti di accesso specifici, chiamare le *Impostazioni*. metodo **requestMediaAccessRights** , passando un parametro che specifica il livello richiesto.</span><span class="sxs-lookup"><span data-stu-id="94604-118">To request specific access rights, call the *Settings*.**requestMediaAccessRights** method, passing a parameter that specifies the level you are requesting.</span></span> <span data-ttu-id="94604-119">Il metodo Visualizza un messaggio all'utente che descrive il livello di accesso richiesto e restituisce un valore **booleano** che indica se l'accesso è stato concesso.</span><span class="sxs-lookup"><span data-stu-id="94604-119">The method displays a message to the user explaining the requested level of access, and returns a **Boolean** value indicating whether the access was granted.</span></span>

<span data-ttu-id="94604-120">Determinati diritti di accesso vengono concessi automaticamente in base alla posizione in cui il codice è in esecuzione rispetto al computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="94604-120">Certain access rights are granted automatically depending on where your code is running relative to the user's computer.</span></span>

-   <span data-ttu-id="94604-121">Se la pagina Web o il programma si trova nel computer dell'utente, per impostazione predefinita vengono concessi i diritti di accesso completi.</span><span class="sxs-lookup"><span data-stu-id="94604-121">If your webpage or program is located on the user's computer, full access rights are granted by default.</span></span>
-   <span data-ttu-id="94604-122">Le pagine Web hanno accesso in lettura al *lettore*. **currentMedia**, *Player*. **currentPlaylist** e *supporti*. **sourceURL** quando la pagina Web si trova in un'area di sicurezza di Internet Explorer che è uguale o meno limitata rispetto all'area di sicurezza dell'elemento multimediale o della playlist.</span><span class="sxs-lookup"><span data-stu-id="94604-122">Web pages have read access to *Player*.**currentMedia**, *Player*.**currentPlaylist**, and *Media*.**sourceURL** when the webpage is located in an Internet Explorer security zone that is the same as or less restricted than the security zone of the media item or playlist.</span></span>

    <span data-ttu-id="94604-123">Le aree di sicurezza sono la zona **attendibile** (incluso il computer locale dell'utente), l'area **Intranet locale** , l'area **Internet** e la zona **limitata** .</span><span class="sxs-lookup"><span data-stu-id="94604-123">Ranging from least restricted to most restricted, the security zones are the **Trusted** zone (including the user's local computer), the **Local intranet** zone, the **Internet** zone, and the **Restricted** zone.</span></span>

    <span data-ttu-id="94604-124">Ad esempio, una pagina Web dell'area **Intranet locale** dispone di diritti di accesso completi al *lettore*. **currentMedia** quando l'elemento multimediale corrispondente si trova nella Intranet locale o in Internet, ma è necessario richiedere i diritti di accesso per gli elementi multimediali presenti nel computer locale di un utente o in un sito Web nell'area **attendibile** .</span><span class="sxs-lookup"><span data-stu-id="94604-124">For example, a webpage in the **Local intranet** zone has full access rights to *Player*.**currentMedia** when the corresponding media item is on the local intranet or the Internet, but access rights must be requested for media items located on a user's local computer or on a website in the **Trusted** zone.</span></span>

<span data-ttu-id="94604-125">È necessario testare l'applicazione basata su Web o basata su Windows in tutte le aree di sicurezza che possono verificarsi.</span><span class="sxs-lookup"><span data-stu-id="94604-125">You should test your Web-based or Windows-based application in all of the security zones it may encounter.</span></span> <span data-ttu-id="94604-126">L'applicazione deve essere progettata per gestire il rifiuto di una richiesta di accesso in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="94604-126">The application should be designed to handle denial of an access request correctly.</span></span>

<span data-ttu-id="94604-127">Le versioni del modello a oggetti di Windows Media Player precedenti alla serie Windows Media Player 9 non includono **mediaAccessRights** o **requestMediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="94604-127">Windows Media Player object model versions prior to Windows Media Player 9 Series do not include **mediaAccessRights** or **requestMediaAccessRights**.</span></span> <span data-ttu-id="94604-128">Queste versioni precedenti di Windows Media Player consentono all'utente di impostare i livelli di accesso utilizzando la finestra di dialogo **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="94604-128">These earlier versions of Windows Media Player enable the user to set access levels using the **Options** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94604-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94604-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94604-130">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="94604-130">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="94604-131">**Utilizzo della libreria**</span><span class="sxs-lookup"><span data-stu-id="94604-131">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




