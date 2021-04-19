---
description: Quando si accede a un server di Strumentazione gestione Windows (WMI) con uno script, è possibile scegliere tra i protocolli di autenticazione NT LAN Manager (NTLM) o Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Impostazione del servizio di autenticazione tramite VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318523"
---
# <a name="setting-the-authentication-service-using-vbscript"></a><span data-ttu-id="a3995-103">Impostazione del servizio di autenticazione tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="a3995-103">Setting the Authentication Service Using VBScript</span></span>

<span data-ttu-id="a3995-104">Quando si accede a un server di Strumentazione gestione Windows (WMI) con uno script, è possibile scegliere tra i protocolli di autenticazione NT LAN Manager (NTLM) o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a3995-104">When accessing a Windows Management Instrumentation (WMI) server with a script, you can choose between NT LAN Manager (NTLM) or Kerberos authentication protocols.</span></span> <span data-ttu-id="a3995-105">Non è necessario specificare Kerberos tranne quando si usa la delega.</span><span class="sxs-lookup"><span data-stu-id="a3995-105">Specifying Kerberos is not required except when using delegation.</span></span> <span data-ttu-id="a3995-106">Per ulteriori informazioni, vedere [la pagina relativa alla connessione a una terza delega del computer](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="a3995-106">For more information, see [Connecting to a 3rd Computer-Delegation](connecting-to-a-3rd-computer-delegation.md).</span></span>

<span data-ttu-id="a3995-107">Poiché le versioni del sistema operativo sono diverse da quelle usate dal servizio di autenticazione, è consigliabile non specificare un valore per il campo Authority quando ci si connette a un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="a3995-107">Because operating system versions differ in which authentication service they use, it is recommended that you do not specify a value for the authority field when connecting to a remote system.</span></span> <span data-ttu-id="a3995-108">Al contrario, consentire al sistema operativo e alla versione distribuita di Component Object Model (DCOM) di selezionare NTLM o Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a3995-108">Instead, allow the operating system and distributed version of Component Object Model (DCOM) to select NTLM or Kerberos.</span></span> <span data-ttu-id="a3995-109">Se viene specificato un servizio di autenticazione, la sintassi richiede il nome dell'entità server, ovvero il nome del computer di destinazione invece del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="a3995-109">If an authentication service is specified, the syntax requires the server principal name, which is the name of the target computer rather than the domain controller.</span></span>

<span data-ttu-id="a3995-110">È possibile utilizzare il parametro Authority solo con connessioni a server WMI remoti.</span><span class="sxs-lookup"><span data-stu-id="a3995-110">You can use the authority parameter only with connections to remote WMI servers.</span></span> <span data-ttu-id="a3995-111">Il tentativo di connessione non riesce se si tenta di impostare i livelli di autorizzazione come parte di un moniker o con una chiamata a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) per una connessione locale.</span><span class="sxs-lookup"><span data-stu-id="a3995-111">The connection attempt fails if you attempt to set authorization levels as part of a moniker or with a call to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) for a local connection.</span></span>

<span data-ttu-id="a3995-112">Eseguire la procedura seguente per specificare il servizio di autenticazione che si desidera utilizzare nel parametro *strAuthority* del metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) o la connessione alla stringa del [moniker](constructing-a-moniker-string.md) .</span><span class="sxs-lookup"><span data-stu-id="a3995-112">Perform the following procedure to specify the authentication service that you want to use in the *strAuthority* parameter of the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method or the [moniker](constructing-a-moniker-string.md) string connection.</span></span>

<span data-ttu-id="a3995-113">**Per specificare l'autenticazione NTLM o Kerberos con l'API di scripting per WMI**</span><span class="sxs-lookup"><span data-stu-id="a3995-113">**To specify NTLM or Kerberos authentication with the Scripting API for WMI**</span></span>

1.  <span data-ttu-id="a3995-114">Se il parametro *strAuthority* inizia con la stringa "Kerberos:", WMI presuppone che la stringa faccia riferimento a un nome di entità Kerberos e venga utilizzata l'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a3995-114">If the *strAuthority* parameter begins with the string "kerberos:", WMI assumes the string refers to a Kerberos principal name and Kerberos authentication is used.</span></span> <span data-ttu-id="a3995-115">Se il parametro *strAuthority* inizia con la stringa "ntlmdomain:", WMI utilizza invece l'autenticazione NTLM.</span><span class="sxs-lookup"><span data-stu-id="a3995-115">If the *strAuthority* parameter begins with the string "ntlmdomain:", WMI uses NTLM authentication instead.</span></span>
2.  <span data-ttu-id="a3995-116">In alternativa, è possibile utilizzare la parte autorità di un moniker per specificare il tipo di autenticazione utilizzato per la connessione a WMI.</span><span class="sxs-lookup"><span data-stu-id="a3995-116">Alternately, You can use the authority part of a moniker to specify the type of authentication used to connect to WMI.</span></span> <span data-ttu-id="a3995-117">Per utilizzare l'autenticazione Kerberos quando si utilizza un moniker, includere la stringa "Authority = Kerberos:" seguita dal nome dell'entità.</span><span class="sxs-lookup"><span data-stu-id="a3995-117">To use Kerberos authentication when using a moniker include the string, "authority=kerberos:" followed by the principal name.</span></span> <span data-ttu-id="a3995-118">Per utilizzare l'autenticazione NTLM, includere la stringa "Authority = ntlmdomain:" seguita dal nome di dominio NTLM.</span><span class="sxs-lookup"><span data-stu-id="a3995-118">To use NTLM authentication, include the string, "authority=ntlmdomain:" followed by the NTLM domain name.</span></span>

    <span data-ttu-id="a3995-119">Nell'esempio seguente viene illustrato un moniker che richiede l'autenticazione Kerberos utilizzando l'entità "dominio \\ Server".</span><span class="sxs-lookup"><span data-stu-id="a3995-119">The following example shows you a moniker that requests Kerberos authentication using the principal "mydomain\\server".</span></span>

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    <span data-ttu-id="a3995-120">Al contrario, nell'esempio seguente viene illustrato un moniker che richiede l'autenticazione NTLM utilizzando il dominio "dominio".</span><span class="sxs-lookup"><span data-stu-id="a3995-120">In contrast, the following example shows you a moniker that requests NTLM authentication using the domain "mydomain".</span></span>

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



