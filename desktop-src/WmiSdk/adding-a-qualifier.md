---
description: Un qualificatore è una stringa di dati che fornisce altre informazioni su una classe, un'istanza, una proprietà, un metodo o un parametro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Aggiunta di un qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333c24e89d711a8998c58c6201776d5d4c50cc1107f4c9ca4308d9cc992b44dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557824"
---
# <a name="adding-a-qualifier"></a>Aggiunta di un qualificatore

Un qualificatore è una stringa di dati che fornisce altre informazioni su una classe, un'istanza, una proprietà, un metodo o un parametro.

La definizione di classe seguente è un esempio di una classe derivata con qualificatori di classe.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

I qualificatori possono essere suddivisi in qualificatori standard, qualificatori CIM e qualificatori univoci:

-   Qualificatore standard

    Un qualificatore standard è un qualificatore definito da WMI e comunemente usato nel codice MOF. Ad esempio, i [**qualificatori Dynamic**](dynamic-qualifier.md) [**e Read**](standard-qualifiers.md) sono entrambi qualificatori standard. Per altre informazioni, vedere [Qualificatori WMI](wmi-qualifiers.md).

-   Qualificatore CIM

    Un qualificatore CIM è un qualificatore incluso nella specifica CIM. Anche se si usano qualificatori CIM nel codice MOF, i qualificatori standard sono progettati in modo specifico tenendo presente WMI. Per altre informazioni, vedere la specifica [CIM DMTF.](https://www.dmtf.org/spec/cims.html/)

-   Qualificatore univoco

    Un qualificatore univoco è un qualificatore definito in modo specifico per una nuova classe da un provider di classi. Ad esempio, il [**qualificatore Units**](standard-qualifiers.md) è un qualificatore non standard specifico del provider. È possibile creare qualificatori personalizzati da usare con il provider. Per altre informazioni sulla creazione di un provider, vedere [Sviluppo di un provider WMI](developing-a-wmi-provider.md).

Indipendentemente dal qualificatore, il processo principale da eseguire è l'uso del qualificatore nel codice MOF. Per altre informazioni, vedere [Applicazione di un qualificatore](applying-a-qualifier.md). È possibile descrivere ulteriormente un qualificatore con una descrizione del qualificatore. Un qualificatore contiene altre informazioni sul modo in cui un provider deve usare un qualificatore. Per altre informazioni, vedere [Descrizione di un qualificatore con un qualificatore Flavor.](describing-a-qualifier-with-a-qualifier-flavor.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



