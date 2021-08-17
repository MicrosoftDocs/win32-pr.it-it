---
description: Nell'esempio seguente viene illustrato il codice per ricevere e verificare un messaggio firmato. L'esempio riceve il buffer della firma e le relative dimensioni in SignatureBuffer e SignatureBufferSize, il buffer dei messaggi e le relative dimensioni in MessageBuffer e MessageBufferSize.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Verifica di un messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90850a88ede875ae41549bca79aceb2d7bdea17db6f50eeb1a3a5e6dfb9a921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915090"
---
# <a name="verifying-a-message"></a>Verifica di un messaggio

Nell'esempio seguente viene illustrato il codice per ricevere e verificare un messaggio firmato. L'esempio riceve il buffer della firma e le relative dimensioni in SignatureBuffer e SignatureBufferSize, il buffer dei messaggi e le relative dimensioni in MessageBuffer e MessageBufferSize.

Nell'esempio si presuppone che **siano inizializzate** una variabile SecHandle denominata phContext e una struttura **SOCKET** denominata s. Per le dichiarazioni e le inizializzazioni di queste variabili, vedere Using [SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) e [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md). Questo codice include le chiamate alle funzioni in Secur32.lib, che devono essere incluse tra le librerie di collegamento.


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



 

 



