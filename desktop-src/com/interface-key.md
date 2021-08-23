---
title: Chiave interfaccia
description: Registra le nuove interfacce associando un nome di interfaccia a un ID interfaccia (IID). Deve essere presente una sottochiave IID per ogni nuova interfaccia.
ms.assetid: 2b2b7506-ac42-4bc4-bad5-17be57d6b4f5
keywords:
- Chiave del Registro di sistema dell'interfaccia COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda0cc29331521025a9274dca7b85080be2ddd5a9b631d2660eadaa13fe4941a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048149"
---
# <a name="interface-key"></a>Chiave interfaccia

Registra le nuove interfacce associando un nome di interfaccia a un ID interfaccia (IID). Deve essere presente una sottochiave IID per ogni nuova interfaccia.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ Interfaccia \_ delle classi SOFTWARE \\ \\ \\ LOCAL MACHINE** \\ *{* IID *}*



| Valore del Registro di sistema                               | Descrizione                                                                                            |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**BaseInterface**](baseinterface.md)       | Identifica l'interfaccia da cui deriva l'interfaccia corrente.                                  |
| [**NumMethods**](nummethods.md)             | Contiene il numero di metodi nell'interfaccia associata, inclusi i metodi delle interfacce derivate. |
| [**ProxyStubClsid**](proxystubclsid.md)     | Mappe un IID a un CLSID nelle DLL proxy a 16 bit.                                                           |
| [**ProxyStubClsid32**](proxystubclsid32.md) | Mappe un IID a un CLSID nelle DLL proxy a 32 bit.                                                           |



 

## <a name="remarks"></a>Commenti

La **chiave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corrisponde alla chiave **HKEY CLASSES \_ \_ ROOT,** che è stata mantenuta per garantire la compatibilità con le versioni precedenti di COM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia**](interface.md)
</dt> </dl>

 

 




