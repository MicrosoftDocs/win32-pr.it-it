---
description: Per modificare gli attributi di una connessione, ad esempio il pacchetto di crittografia o l'autenticazione client, è possibile richiedere un &\# 0034; rollforward&\# 0034; o rinegoziazione della connessione.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Rinegoziazione di una connessione Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311612"
---
# <a name="renegotiating-an-schannel-connection"></a><span data-ttu-id="2f1b0-103">Rinegoziazione di una connessione Schannel</span><span class="sxs-lookup"><span data-stu-id="2f1b0-103">Renegotiating an Schannel Connection</span></span>

<span data-ttu-id="2f1b0-104">Per modificare gli attributi di una connessione, ad esempio il pacchetto di crittografia o l'autenticazione client, è possibile richiedere una "ripetizione" o una rinegoziazione della connessione.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-104">To change a connection's attributes, such as the cipher suite or client authentication, you can request a "redo" or renegotiation of the connection.</span></span>

<span data-ttu-id="2f1b0-105">Se gli attributi che si desidera modificare sono controllati da credenziali, è necessario ottenere nuove credenziali prima di rinegoziare la connessione.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-105">If the attributes you want to change are controlled by credentials, you must obtain new credentials before you renegotiate the connection.</span></span> <span data-ttu-id="2f1b0-106">Per ulteriori informazioni, vedere [ottenere le credenziali Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="2f1b0-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

<span data-ttu-id="2f1b0-107">Per richiedere un rollforward da un'applicazione client, chiamare la funzione [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-107">To request a redo from a client application, call the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="2f1b0-108">Le applicazioni server chiamano la funzione [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-108">Server applications call the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="2f1b0-109">Impostare i parametri come segue:</span><span class="sxs-lookup"><span data-stu-id="2f1b0-109">Set the parameters as follows:</span></span>

-   <span data-ttu-id="2f1b0-110">Specificare il [*contesto di sicurezza*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) esistente nel parametro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-110">Specify the existing [*security context*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) in the *phContext* parameter.</span></span>
-   <span data-ttu-id="2f1b0-111">(Solo client) Specificare lo stesso nome server (nel parametro *pszTargetName* ) come specificato durante la definizione del contesto.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-111">(Clients only) Specify the same server name (in the *pszTargetName* parameter) as specified when establishing the context.</span></span>
-   <span data-ttu-id="2f1b0-112">Specificare le nuove credenziali, se applicabile, usando il parametro *phCredential* .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-112">Specify new credentials, using the *phCredential* parameter, if applicable.</span></span>
-   <span data-ttu-id="2f1b0-113">Se si desidera modificare gli attributi del contesto non correlati alle credenziali, specificare questi attributi utilizzando il parametro *fContextReq* .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-113">If you want to change context attributes unrelated to the credentials, specify these attributes using the *fContextReq* parameter.</span></span>

<span data-ttu-id="2f1b0-114">Dopo aver chiamato la funzione appropriata, l'applicazione deve inviare i risultati al client e continuare a elaborare i messaggi in arrivo usando la funzione [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-114">After calling the appropriate function, your application should send the results to the client and continue processing incoming messages using the [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function.</span></span>

<span data-ttu-id="2f1b0-115">La funzione [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) restituirà il \_ secondo \_ rinegoziato quando Schannel è pronto per continuare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-115">The [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function will return SEC\_I\_RENEGOTIATE when Schannel is ready for your application to proceed.</span></span> <span data-ttu-id="2f1b0-116">Quando si riceve la prima volta \_ che si \_ rinegozia il codice restituito, l'applicazione deve chiamare [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (Server) o [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (client) e passare il contenuto di SECBUFFER_EXTRA restituito da DecryptMessage nel SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-116">When you receive the SEC\_I\_RENEGOTIATE return code, your application must call [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servers) or [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clients), and pass the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="2f1b0-117">Quando questa chiamata restituisce un valore, procedere come se l'applicazione creasse una nuova connessione.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-117">After this call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 
