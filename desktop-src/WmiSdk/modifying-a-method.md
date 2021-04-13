---
description: Oltre alle classi e alle istanze, WMI consente di modificare un metodo. Il motivo principale per cui si desidera modificare un metodo è se è stata modificata l'implementazione di un metodo in un provider. Per ulteriori informazioni, vedere scrittura di un provider di metodi.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modifica di un metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401563"
---
# <a name="modifying-a-method"></a>Modifica di un metodo

Oltre alle classi e alle istanze, WMI consente di modificare un metodo. Il motivo principale per cui si desidera modificare un metodo è se è stata modificata l'implementazione di un metodo in un provider. Per ulteriori informazioni, vedere [scrittura di un provider di metodi](writing-a-method-provider.md).

La modifica di un metodo non è un'operazione che può essere eseguita nello script.

Nella procedura riportata di seguito viene descritto come modificare un metodo a livello di codice.

**Per modificare un metodo a livello di codice**

1.  Recuperare la definizione di classe con una chiamata a [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).

    I due parametri out, *ppInSignature* e *ppOutSignature*, contengono rispettivamente la classe in-Parameter e la classe out-parameter. Il valore restituito viene aggregato nella classe del parametro out come proprietà e deve essere denominato **returnValue**.

2.  Recuperare e modificare i parametri con le chiamate a [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)o [**IWbemClassObject::D Elimina**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).
3.  Inserire nuovamente la nuova versione del metodo nella classe padre con una chiamata a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

 

 



