---
description: Quando un client e un server completano la configurazione del contesto di sicurezza, è possibile utilizzare le funzioni di supporto del messaggio.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Firma di un messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316231"
---
# <a name="signing-a-message"></a><span data-ttu-id="e403d-103">Firma di un messaggio</span><span class="sxs-lookup"><span data-stu-id="e403d-103">Signing a Message</span></span>

<span data-ttu-id="e403d-104">Quando un client e un server completano la configurazione del [*contesto di sicurezza*](../secgloss/s-gly.md), è possibile utilizzare le funzioni di supporto del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e403d-104">When a client and server finish setting up the [*security context*](../secgloss/s-gly.md), message support functions can be used.</span></span> <span data-ttu-id="e403d-105">Il client e il server utilizzano il token del contesto di sicurezza creato quando è stata stabilita la sessione per chiamare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="e403d-105">The client and server use the security context token created when the session was established to call [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions.</span></span> <span data-ttu-id="e403d-106">Il token di contesto può essere usato con [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) per la [*privacy*](../secgloss/p-gly.md)delle comunicazioni.</span><span class="sxs-lookup"><span data-stu-id="e403d-106">The context token can be used with [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) for communications [*privacy*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="e403d-107">Nell'esempio seguente viene illustrato il lato client che genera un messaggio firmato da inviare al server.</span><span class="sxs-lookup"><span data-stu-id="e403d-107">The following example shows the client side generating a signed message to send to the server.</span></span> <span data-ttu-id="e403d-108">Prima di chiamare [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), il client chiama [**QueryContextAttributes (generale)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una struttura di [**\_ dimensioni SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) per determinare la lunghezza del buffer necessaria per memorizzare la firma del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e403d-108">Before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the client calls [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) with a [**SecPkgContext\_Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) structure to determine the length of the buffer needed to hold the message signature.</span></span> <span data-ttu-id="e403d-109">Se il membro **cbMaxSignature** è zero, il [*pacchetto di sicurezza*](../secgloss/s-gly.md) non supporta la firma dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="e403d-109">If the **cbMaxSignature** member is zero, the [*security package*](../secgloss/s-gly.md) does not support signing messages.</span></span> <span data-ttu-id="e403d-110">In caso contrario, questo membro indica le dimensioni del buffer da allocare per ricevere la firma.</span><span class="sxs-lookup"><span data-stu-id="e403d-110">Otherwise, this member indicates the size of the buffer to allocate to receive the signature.</span></span>

<span data-ttu-id="e403d-111">Nell'esempio si presuppone che venga inizializzata una variabile **SecHandle** denominata *phContext* e una struttura **socket** denominata *s* .</span><span class="sxs-lookup"><span data-stu-id="e403d-111">The example assumes that a **SecHandle** variable named *phContext* and a **SOCKET** structure named *s* are initialized.</span></span> <span data-ttu-id="e403d-112">Per le dichiarazioni e le inizializzazioni di queste variabili, vedere [uso di SSPI con un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) e [uso di SSPI con un server Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="e403d-112">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="e403d-113">Questo esempio include le chiamate alle funzioni in Secur32. lib, che devono essere incluse tra le librerie di collegamento.</span><span class="sxs-lookup"><span data-stu-id="e403d-113">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



<span data-ttu-id="e403d-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) restituisce **true** se il contesto è configurato per consentire i messaggi di firma e se il descrittore del buffer di input è formattato correttamente.</span><span class="sxs-lookup"><span data-stu-id="e403d-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) returns **TRUE** if the context is set up to allow signing messages and if the input buffer descriptor is correctly formatted.</span></span> <span data-ttu-id="e403d-115">Dopo la firma del messaggio, il messaggio e la firma con le relative lunghezze vengono inviati al computer remoto.</span><span class="sxs-lookup"><span data-stu-id="e403d-115">After the message is signed, the message and the signature with their lengths are sent to the remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="e403d-116">Il contenuto dei dati delle strutture [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) viene inviato, non le strutture **SecBuffer** né la struttura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="e403d-116">The data contents of the [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures are sent, not the **SecBuffer** structures themselves nor the [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="e403d-117">Le nuove strutture **SecBuffer** e una nuova struttura **SecBufferDesc** vengono create dall'applicazione ricevente per verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="e403d-117">New **SecBuffer** structures and a new **SecBufferDesc** structure are created by the receiving application to verify the signature.</span></span>

 

 

 
