---
description: Nell'esempio seguente viene illustrato un messaggio crittografato prima di essere inviato a un computer remoto tramite la connessione protetta.
ms.assetid: 1788b496-ad19-427e-be07-4aa68543fced
title: Crittografia di un messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fcc987e17c37f9b2eb80289f257101b51f5f3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878626"
---
# <a name="encrypting-a-message"></a>Crittografia di un messaggio

Nell'esempio seguente viene illustrato un messaggio crittografato prima di essere inviato a un computer remoto tramite la connessione protetta.

Nell'esempio si presuppone che venga inizializzata una variabile **SecHandle** denominata `phContext` e un **socket** denominato `s` . Per le dichiarazioni e le inizializzazioni di queste variabili, vedere [uso di SSPI con un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) e [uso di SSPI con un server Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Questo esempio include le chiamate alle funzioni in Secur32. lib, che devono essere incluse tra le librerie di collegamento.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_StreamSizes  Sizes;
SECURITY_STATUS            scRet;
SecBufferDesc              Message;
SecBuffer                  Buffers[4];
SecBuffer                  *pDataBuffer;

PBYTE                       pbIoBuffer;
DWORD                       cbIoBuffer;
DWORD                       cbIoBufferLength;
PBYTE                       pbMessage;
DWORD                       cbMessage;

//--------------------------------------------------------------------
// Get the stream encryption sizes. This needs to 
// be done once per connection. 
// phContext must have been initialized during the handshake process.

scRet = QueryContextAttributes(
            phContext,
            SECPKG_ATTR_STREAM_SIZES,
            &Sizes);

if(FAILED(scRet))
{
    MyHandleError("Error reading SECPKG_ATTR_STREAM_SIZES");
}

//--------------------------------------------------------------------
// Allocate a working buffer. The plaintext sent to EncryptMessage
// can never be more than 'Sizes.cbMaximumMessage', so a buffer 
// size of Sizes.cbMaximumMessage plus the header and trailer sizes 
// is sufficient for the longest message.

cbIoBufferLength = Sizes.cbHeader + 
                   Sizes.cbMaximumMessage +
                   Sizes.cbTrailer;

if(!(pbIoBuffer = malloc((BYTE *), cbIoBufferLength)))
{
    MyHandleError("Out of memory");
}

//--------------------------------------------------------------------
// Create a plaintext message to be encrypted offset into the data 
// buffer by "header size" bytes. This allows encryption in place.

pbMessage = pbIoBuffer + Sizes.cbHeader;

StringCbPrintfA(pbMessage,
                cbIoBufferLength - Sizes.cbHeader,
                "This is the plaintext message.");
cbMessage = strlen(pbMessage);

//--------------------------------------------------------------------
// Encrypt the plaintext message.

Buffers[0].pvBuffer     = pbIoBuffer;
Buffers[0].cbBuffer     = Sizes.cbHeader;
Buffers[0].BufferType   = SECBUFFER_STREAM_HEADER;

Buffers[1].pvBuffer     = pbMessage;
Buffers[1].cbBuffer     = cbMessage;
Buffers[1].BufferType   = SECBUFFER_DATA;

Buffers[2].pvBuffer     = pbMessage + cbMessage;
Buffers[2].cbBuffer     = Sizes.cbTrailer;
Buffers[2].BufferType   = SECBUFFER_STREAM_TRAILER;

Buffers[3].BufferType   = SECBUFFER_EMPTY;

Message.ulVersion       = SECBUFFER_VERSION;
Message.cBuffers        = 4;
Message.pBuffers        = Buffers;

scRet = EncryptMessage(phContext, 0, &Message, 0);

if(FAILED(scRet))
{
    MyHandleError("Error returned by EncryptMessage.");
}

//--------------------------------------------------------------------
// Send the encrypted data.

if(!(SendMsg(
     s,
     pbIoBuffer,
     Buffers[0].cbBuffer + Buffers[1].cbBuffer + 
           Buffers[2].cbBuffer)))
{
     MyHandleError("SendMsg failed.");
}
```



 

 



