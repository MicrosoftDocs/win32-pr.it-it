---
description: Oltre alle classi e alle istanze, WMI consente di modificare un metodo. Il motivo principale per cui si vuole modificare un metodo è se è stata modificata l'implementazione di un metodo in un provider. Per altre informazioni, vedere Scrittura di un provider di metodi.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modifica di un metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9d780bad44ff89365041a2388fbdf01c1ddd8cc630b278ea6af7abd7ae4f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992851"
---
# <a name="modifying-a-method"></a>Modifica di un metodo

Oltre alle classi e alle istanze, WMI consente di modificare un metodo. Il motivo principale per cui si vuole modificare un metodo è se è stata modificata l'implementazione di un metodo in un provider. Per altre informazioni, vedere [Scrittura di un provider di metodi.](writing-a-method-provider.md)

La modifica di un metodo non è un'operazione che può essere eseguita nello script.

Nella procedura seguente viene descritto come modificare un metodo a livello di codice.

**Per modificare un metodo a livello di codice**

1.  Recuperare la definizione della classe con una chiamata a [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    I due parametri out, *ppInSignature* e *ppOutSignature*, contengono rispettivamente la classe in-parameter e la classe out-parameter. Il valore restituito viene aggregato nella classe out-parameter come proprietà e deve essere denominato **ReturnValue.**

2.  Recuperare e modificare i parametri con chiamate a [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)o [**IWbemClassObject::D elete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Inserire di nuovo la nuova versione del metodo nella classe padre con una chiamata a [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze.](manipulating-class-and-instance-information.md)

 

 



