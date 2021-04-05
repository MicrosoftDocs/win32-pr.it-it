---
title: Chiave interfaccia
description: Registra le nuove interfacce associando il nome di un'interfaccia a un ID di interfaccia (IID). Deve essere presente una sottochiave IID per ogni nuova interfaccia.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Chiave del registro di sistema Interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ae31de7af534a58b4973629f2b889f3332047f6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045073"
---
# <a name="interface-key"></a>Chiave interfaccia

Registra le nuove interfacce associando il nome di un'interfaccia a un ID di interfaccia (IID). Deve essere presente una sottochiave IID per ogni nuova interfaccia.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ \_Interfaccia delle \\ \\ classi software \\ del computer locale** \\ *{* IID *}*



| Valore del Registro di sistema                               | Descrizione                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifica l'interfaccia da cui deriva l'interfaccia corrente.                                  |
| [**NumMethods**](nummethods.md)             | Contiene il numero di metodi nell'interfaccia associata, inclusi i metodi delle interfacce derivate. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Esegue il mapping di un IID a un CLSID nelle DLL proxy a 16 bit.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Esegue il mapping di un IID a un CLSID in DLL proxy a 32 bit.                                                           |



 

## <a name="remarks"></a>Commenti

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia**](interface.md)
</dt> </dl>

 

 




