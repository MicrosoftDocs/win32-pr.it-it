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
# <a name="signing-a-message"></a>Firma di un messaggio

Quando un client e un server completano la configurazione del [*contesto di sicurezza*](../secgloss/s-gly.md), è possibile utilizzare le funzioni di supporto del messaggio. Il client e il server utilizzano il token del contesto di sicurezza creato quando è stata stabilita la sessione per chiamare le funzioni [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) e [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . Il token di contesto può essere usato con [**EncryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) e [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) per la [*privacy*](../secgloss/p-gly.md)delle comunicazioni.

Nell'esempio seguente viene illustrato il lato client che genera un messaggio firmato da inviare al server. Prima di chiamare [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), il client chiama [**QueryContextAttributes (generale)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una struttura di [**\_ dimensioni SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) per determinare la lunghezza del buffer necessaria per memorizzare la firma del messaggio. Se il membro **cbMaxSignature** è zero, il [*pacchetto di sicurezza*](../secgloss/s-gly.md) non supporta la firma dei messaggi. In caso contrario, questo membro indica le dimensioni del buffer da allocare per ricevere la firma.

Nell'esempio si presuppone che venga inizializzata una variabile **SecHandle** denominata *phContext* e una struttura **socket** denominata *s* . Per le dichiarazioni e le inizializzazioni di queste variabili, vedere [uso di SSPI con un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) e [uso di SSPI con un server Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Questo esempio include le chiamate alle funzioni in Secur32. lib, che devono essere incluse tra le librerie di collegamento.


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



[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) restituisce **true** se il contesto è configurato per consentire i messaggi di firma e se il descrittore del buffer di input è formattato correttamente. Dopo la firma del messaggio, il messaggio e la firma con le relative lunghezze vengono inviati al computer remoto.

> [!Note]  
> Il contenuto dei dati delle strutture [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) viene inviato, non le strutture **SecBuffer** né la struttura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) . Le nuove strutture **SecBuffer** e una nuova struttura **SecBufferDesc** vengono create dall'applicazione ricevente per verificare la firma.

 

 

 
