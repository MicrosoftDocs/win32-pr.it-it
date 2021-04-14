---
description: Nell'esempio seguente viene illustrato il codice per la ricezione e la verifica di un messaggio firmato. Nell'esempio vengono ricevuti il buffer della firma e le relative dimensioni in SignatureBuffer e SignatureBufferSize e il buffer dei messaggi e le relative dimensioni in MessageBuffer e MessageBufferSize.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Verifica di un messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebf62be707efcbd3ab3a5eca5345261ca1a0fde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343171"
---
# <a name="verifying-a-message"></a>Verifica di un messaggio

Nell'esempio seguente viene illustrato il codice per la ricezione e la verifica di un messaggio firmato. Nell'esempio vengono ricevuti il buffer della firma e le relative dimensioni in SignatureBuffer e SignatureBufferSize e il buffer dei messaggi e le relative dimensioni in MessageBuffer e MessageBufferSize.

Nell'esempio si presuppone che venga inizializzata una variabile **SecHandle** denominata phContext e una struttura **socket** denominata s. Per le dichiarazioni e le inizializzazioni di queste variabili, vedere [uso di SSPI con un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) e [uso di SSPI con un server Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Questo codice include le chiamate alle funzioni in Secur32. lib, che devono essere incluse tra le librerie di collegamento.


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



