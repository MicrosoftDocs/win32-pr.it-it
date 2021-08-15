---
description: La funzione CreateProtocol notifica Network Monitor che esiste un parser di protocollo specifico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Funzione CreateProtocol (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 173f744406ef2b360c0af7158e397c2001f146b9f2339bf6aaf3468b9a1465dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796352"
---
# <a name="createprotocol-function"></a>Funzione CreateProtocol

La **funzione CreateProtocol** notifica Network Monitor che esiste un parser di protocollo specifico.

## <a name="syntax"></a>Sintassi


```C++
HPROTOCOL WINAPI CreateProtocol(
  _In_ LPSTR         ProtocolName,
  _In_ LPENTRYPOINTS lpEntryPoints,
  _In_ DWORD         cbEntryPoints
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProtocolName* \[ Pollici\]
</dt> <dd>

Nome del protocollo rilevato dal parser.

</dd> <dt>

*lpEntryPoints* \[ Pollici\]
</dt> <dd>

Struttura [ENTRYPOINTS](entrypoints.md) che contiene i punti di ingresso dll del parser rimanenti. Per un elenco delle funzioni di esportazione a cui fa riferimento ogni punto di ingresso, vedere Note. I punti di ingresso devono essere specificati nell'ordine specificato dalla struttura **ENTRYPOINTS.**

</dd> <dt>

*cbEntryPoints* \[ Pollici\]
</dt> <dd>

Dimensioni della struttura **ENTRYPOINTS.** Network Monitor fornisce una macro ENTRYPOINTS SIZE che è possibile \_ usare per specificare le dimensioni della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il protocollo.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

La DLL del parser chiama **CreateProtocol durante** l'implementazione di [DllMain](dllmain-parser.md). La **funzione CreateProtocol** viene chiamata quando il sistema operativo carica la DLL del parser per la prima volta.

I punti di ingresso a cui si fa riferimento nel parametro *lpEntryPoints* includono puntatori alle funzioni di esportazione seguenti che devono essere fornite nell'ordine presentato qui.

-   [Registra](register-parser.md)
-   [Annullamento registrazione](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [Proprietà FormatProperties](formatproperties.md)



| Per informazioni su                                                                                 | Vedere                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor.                                          | [Parser](parsers.md)                                  |
| Come implementare **DllMain** include un esempio di chiamata **a CreateProtocol all'interno** **di DllMain**. | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

