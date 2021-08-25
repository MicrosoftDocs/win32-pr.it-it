---
description: La funzione di esportazione DllMain per il parser identifica l'esistenza del parser e rilascia le risorse Network Monitor per il parser. DllMain deve essere implementato in tutte le DLL del parser.
ms.assetid: 2ce79d49-3aad-461f-99cf-cf632680efcc
title: Funzione di callback del parser DllMain (Process.h)
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
ms.openlocfilehash: 5df58ef86971fcf60e79fbae8e92313dbd0b0371e2311cc30b494950e4f37dd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890841"
---
# <a name="dllmain-parser-callback-function"></a>Funzione di callback del parser DllMain

La funzione di esportazione **DllMain** per il parser identifica l'esistenza del parser e rilascia le risorse Network Monitor per il parser. **DllMain** deve essere implementato in tutte le DLL del parser.

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

*hInstance* \[ Pollici\]
</dt> <dd>

Handle a un'istanza del parser.

</dd> <dt>

*Comando* \[ Pollici\]
</dt> <dd>

Indicatore per determinare il motivo per cui viene chiamata la funzione. Per un elenco di tutti i flag possibili, vedere [DllMain](/windows/desktop/Dlls/dllmain). L'implementazione del parser deve elaborare i valori seguenti.



| Valore                                                                                                                                                                         | Significato                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**DLL \_ PROCESS \_ ATTACH**</dt> </dl> | Quando **dllMain** viene chiamato per la prima volta, la DLL deve chiamare [CreateProtocol](createprotocol.md) per fornire informazioni Network Monitor. <br/>   |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**SCOLLEGAMENTO \_ DEL PROCESSO \_ DLL**</dt> </dl> | Quando **dllMain viene** chiamato per l'ultima volta, la DLL deve chiamare [DestroyProtocol](destroyprotocol.md) per rilasciare le risorse utilizzate dalla DLL. <br/> |



 

</dd> <dt>

*Reserved* 
</dt> <dd>

Non usato ora.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La DLL del parser restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Il sistema operativo chiama **DllMain** per caricare e scaricare la DLL del parser. Questa funzione è basata sulla funzione [DllMain](/windows/desktop/Dlls/dllmain) della libreria a collegamento dinamico.

È anche possibile usare l'implementazione di **DllMain** per archiviare un'istanza di un parser da usare in futuro. Ad esempio, è possibile archiviare un'istanza dll del parser e quindi usarla per una chiamata di sistema in futuro.



| Per informazioni su                                        | Vedere                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                  |
| Punti di ingresso inclusi nella DLL del parser.        | [Architettura della DLL del parser](parser-dll-architecture.md)  |
| Come implementare **DllMain**  è incluso un esempio.        | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Process.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CreateProtocol](createprotocol.md)
</dt> <dt>

[DestroyProtocol](destroyprotocol.md)
</dt> <dt>

[DllMain](/windows/desktop/Dlls/dllmain)
</dt> </dl>

 

