---
description: La funzione di esportazione ParserAutoInstallInfo identifica il parser o i parser che si trovano in una DLL. ParserAutoInstallInfo deve essere implementato in tutte le DLL del parser.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Funzione di callback ParserAutoInstallInfo (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParserAutoInstallInfo
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3c6c69b66f3ff92905333a28c5dadfd79290033f0abb68cb2a790f07c6e34412
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063752"
---
# <a name="parserautoinstallinfo-callback-function"></a>Funzione di callback ParserAutoInstallInfo

La **funzione di esportazione ParserAutoInstallInfo** identifica il parser o i parser che si trovano in una DLL. **ParserAutoInstallInfo** deve essere implementato in tutte le DLL del parser.

## <a name="syntax"></a>Sintassi


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parametri

Questa funzione di callback non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è una [struttura PF \_ PARSERDLLINFO](pf-parserdllinfo.md) che descrive i parser nella DLL.

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Quando Network Monitor carica per la prima volta, chiama **ParserAutoInstallInfo** (se esistente) per installare automaticamente ogni parser e quindi enumerare tutte le DLL del parser nella sottodirectory del parser.

Le informazioni restituite nella **struttura PF \_ PARSERDLLINFO** includono quanto segue:

-   Numero di parser nella DLL (in genere uno).
-   Nome e breve descrizione del protocollo rilevato da ogni parser.
-   Un file della Guida facoltativo per ogni protocollo.
-   Protocolli che precedono ogni protocollo.
-   Protocolli che seguono ogni protocollo.

Ogni DLL del parser deve contenere un parser. Tuttavia, Network Monitor consente di creare una DLL che contiene più parser. Ad esempio, tcpip.dll è una DLL Network Monitor con più parser.



| Per informazioni su                                               | Vedere                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor.        | [Parser](parsers.md)                                                       |
| Punti di ingresso inclusi nella DLL del parser.               | [Architettura della DLL del parser](parser-dll-architecture.md)                       |
| Come implementare **ParserAutoInstallInfo**  include un esempio. | [Implementazione di ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




