---
description: La funzione di esportazione ParserAutoInstallInfo identifica il parser o i parser che si trovano in una DLL. ParserAutoInstallInfo deve essere implementato in tutte le dll del parser.
ms.assetid: 7af3bf3c-d415-4af9-8f5c-c9a76535bd1a
title: Funzione di callback ParserAutoInstallInfo (Netmon. h)
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
ms.openlocfilehash: 7702ae8aad5ae24acf3835451b7b8eff3a26ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342741"
---
# <a name="parserautoinstallinfo-callback-function"></a>Funzione di callback ParserAutoInstallInfo

La funzione di esportazione **ParserAutoInstallInfo** identifica il parser o i parser che si trovano in una dll. **ParserAutoInstallInfo** deve essere implementato in tutte le dll del parser.

## <a name="syntax"></a>Sintassi


```C++
PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo(void);
```



## <a name="parameters"></a>Parametri

Questa funzione di callback non ha parametri.

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è una struttura [PF \_ PARSERDLLINFO](pf-parserdllinfo.md) che descrive i parser nella dll.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Quando Network Monitor viene caricato per la prima volta, viene chiamato **ParserAutoInstallInfo** (se esiste) per installare automaticamente ogni parser e quindi vengono enumerate tutte le dll del parser nella sottodirectory del parser.

Le informazioni restituite nella struttura **PF \_ PARSERDLLINFO** includono quanto segue:

-   Numero di parser nella DLL (in genere uno).
-   Nome e breve descrizione del protocollo rilevato da ogni parser.
-   File della guida facoltativo per ogni protocollo.
-   Protocolli che precedono ogni protocollo.
-   Protocolli che seguono ogni protocollo.

Ogni DLL del parser deve contenere un parser. Tuttavia, Network Monitor consente di creare una DLL che contiene più di un parser. Ad esempio, tcpip.dll è un Network Monitor DLL con più di un parser.



| Per informazioni su                                               | Vedere                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor.        | [Parser](parsers.md)                                                       |
| I punti di ingresso inclusi nella DLL del parser.               | [Architettura DLL parser](parser-dll-architecture.md)                       |
| L'implementazione di **ParserAutoInstallInfo**  include un esempio. | [Implementazione di ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




