---
UID: NF:ntw.EtwEventUnregister
title: EtwEventUnregister (funzione)
description: Annulla la registrazione di un evento.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e61de5aa1c050aedd2c82dec471765baa7e6cdd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117687"
---
# <a name="etweventunregister-function"></a>EtwEventUnregister (funzione)


## <a name="description"></a>Descrizione


<b>EtwEventUnregister</b> Annulla la registrazione di un evento.
            

I provider possono chiamare questa funzione solo dalla relativa funzione <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> .


## <a name="parameters"></a>Parametri




### <a name="reghandle-in"></a>RegHandle [in]

Handle per un evento.


## <a name="returns"></a>Restituisce



Restituisce un valore HRESULT.





## <a name="remarks"></a>Commenti



## <a name="see-also"></a>Vedere anche