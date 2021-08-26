---
title: Appendice C DISPID IAccessible
description: Un DISPID consente all'implementazione di IDispatch di cercare i vari metodi e proprietà di un'interfaccia duale.
ms.assetid: 3d19b37a-1ce4-4f34-96b3-ff39b320e8db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f73b1e280a6735f4d7d18f519e60102c04103d9500a588ef0613fd123557ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998881"
---
# <a name="appendix-c-iaccessible-dispids"></a>Appendice C: DISPID IAccessible

Un DISPID consente all'implementazione [**di IDispatch**](idispatch-interface.md) di cercare i vari metodi e proprietà di un'interfaccia duale.


```C++
// PROPERTIES: Hierarchical 
#define DISPID_ACC_PARENT                   (-5000)
#define DISPID_ACC_CHILDCOUNT               (-5001)
#define DISPID_ACC_CHILD                    (-5002)
                                             
// PROPERTIES: Descriptive 
#define DISPID_ACC_NAME                     (-5003)
#define DISPID_ACC_VALUE                    (-5004)
#define DISPID_ACC_DESCRIPTION              (-5005)
#define DISPID_ACC_ROLE                     (-5006)
#define DISPID_ACC_STATE                    (-5007)
#define DISPID_ACC_HELP                     (-5008)
#define DISPID_ACC_HELPTOPIC                (-5009)
#define DISPID_ACC_KEYBOARDSHORTCUT         (-5010)
#define DISPID_ACC_FOCUS                    (-5011)
#define DISPID_ACC_SELECTION                (-5012)
#define DISPID_ACC_DEFAULTACTION            (-5013)

// METHODS 
#define DISPID_ACC_SELECT                   (-5014)
#define DISPID_ACC_LOCATION                 (-5015)
#define DISPID_ACC_NAVIGATE                 (-5016)
#define DISPID_ACC_HITTEST                  (-5017)
#define DISPID_ACC_DODEFAULTACTION          (-5018)
```



 

 




