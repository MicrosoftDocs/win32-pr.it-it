---
description: La funzione CreateProtocol notifica Network Monitor che esiste un parser di protocollo specifico.
ms.assetid: 13ae261f-b1c0-4afc-b718-d64b3d4ec5ee
title: Funzione CreateProtocol (Netmon. h)
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
ms.openlocfilehash: 0b35f9505758256750ae02d24d6c2a84ed0646b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131858"
---
# <a name="createprotocol-function"></a>CreateProtocol (funzione)

La funzione **CreateProtocol** notifica Network Monitor che esiste un parser di protocollo specifico.

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

*ProtocolName* \[ in\]
</dt> <dd>

Nome del protocollo rilevato dal parser.

</dd> <dt>

*lpEntryPoints* \[ in\]
</dt> <dd>

Struttura [ENTRYPOINTS](entrypoints.md) che contiene i punti di ingresso rimanenti della dll del parser. Vedere la sezione Osservazioni per un elenco delle funzioni di esportazione a cui fa riferimento ogni punto di ingresso. I punti di ingresso devono essere specificati nell'ordine specificato dalla struttura **ENTRYPOINTS** .

</dd> <dt>

*cbEntryPoints* \[ in\]
</dt> <dd>

Dimensione della struttura **ENTRYPOINTS** . Network Monitor fornisce una \_ macro di dimensioni ENTRYPOINTS che è possibile usare per specificare le dimensioni della struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un handle per il protocollo.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

La DLL del parser chiama **CreateProtocol** durante la relativa implementazione di [DllMain](dllmain-parser.md). La funzione **CreateProtocol** viene chiamata quando il sistema operativo carica la dll del parser per la prima volta.

I punti di ingresso a cui viene fatto riferimento nel parametro *lpEntryPoints* includono i puntatori alle funzioni di esportazione seguenti che devono essere fornite nell'ordine presentato qui.

-   [Registra](register-parser.md)
-   [Annullamento registrazione](deregister.md)
-   [RecognizeFrame](recognizeframe.md)
-   [AttachProperties](attachproperties.md)
-   [FormatProperties](formatproperties.md)



| Per informazioni su                                                                                 | Vedere                                                     |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor.                                          | [Parser](parsers.md)                                  |
| Come implementare **DllMain** include un esempio di chiamata a **CreateProtocol** all'interno di **DllMain**. | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

