---
description: La funzione di esportazione DllMain per il parser identifica l'esistenza del parser e rilascia le risorse utilizzate da Network Monitor per il parser. DllMain deve essere implementato in tutte le dll del parser.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Funzione di callback del parser DllMain (Process. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 1db69d51f3a46bbe219ef7f7bdea67e8e8970e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314176"
---
# <a name="dllmain-parser-callback-function"></a>Funzione di callback del parser DllMain

La funzione di esportazione **DllMain** per il parser identifica l'esistenza del parser e rilascia le risorse utilizzate da Network Monitor per il parser. **DllMain** deve essere implementato in tutte le dll del parser.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DllMain(
  _In_ HANDLE hInstance,
  _In_ ULONG  Command,
       LPVOID Reserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HINSTANCE* \[ in\]
</dt> <dd>

Handle per un'istanza del parser.

</dd> <dt>

*Comando* \[ in\]
</dt> <dd>

Indicatore per determinare il motivo per cui viene chiamata la funzione. Per un elenco di tutti i flag possibili, vedere [DllMain](/windows/desktop/Dlls/dllmain). L'implementazione del parser deve elaborare i valori seguenti.



| Valore                                                                                                                                                                         | Significato                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**\_connessione processo \_ dll**</dt> </dl> | Quando **DllMain** viene chiamato per la prima volta, è necessario che la dll chiami [CreateProtocol](createprotocol.md) per fornire informazioni a Network Monitor. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**\_ \_ scollegamento processo dll**</dt> </dl> | Quando **DllMain** viene chiamato per l'ultima volta, è necessario che la dll chiami [DestroyProtocol](destroyprotocol.md) per rilasciare le risorse utilizzate dalla dll. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

Non usato adesso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La DLL del parser restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Il sistema operativo chiama **DllMain** per caricare e scaricare la dll del parser. Questa funzione è basata sulla funzione [DllMain](/windows/desktop/Dlls/dllmain) della libreria a collegamento dinamico.

È inoltre possibile utilizzare l'implementazione di **DllMain** per archiviare un'istanza di un parser da utilizzare in futuro. Ad esempio, è possibile archiviare un'istanza di DLL del parser e quindi utilizzarla per una chiamata di sistema in futuro.



| Per informazioni su                                        | Vedere                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                  |
| I punti di ingresso inclusi nella DLL del parser.        | [Architettura DLL parser](parser-dll-architecture.md)  |
| Come implementare **DllMain**  include un esempio.        | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Elabora. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

