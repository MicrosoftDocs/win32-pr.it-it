---
description: Un qualificatore è una stringa di dati che fornisce ulteriori informazioni su una classe, un'istanza, una proprietà, un metodo o un parametro.
ms.assetid: 6984b575-b365-49dd-aeab-a763430f434c
ms.tgt_platform: multiple
title: Aggiunta di un qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a6f18f2b79bcd25b2b4ca75811157c9091e6eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319806"
---
# <a name="adding-a-qualifier"></a>Aggiunta di un qualificatore

Un qualificatore è una stringa di dati che fornisce ulteriori informazioni su una classe, un'istanza, una proprietà, un metodo o un parametro.

La definizione di classe seguente è un esempio di classe derivata con qualificatori di classe.

``` syntax
[Dynamic, Provider ("ProviderX")] 
class MyDerivedClass : MyClass
{
    [key] string sKey;
    [Implemented] sint32 ValueMethod();
    [Implemented] sint32 MyMethod ([in, Id(0)] sint32 Param);
};
```

I qualificatori possono essere divisi in qualificatori standard, qualificatori CIM e qualificatori esclusivi includono quanto segue:

-   Qualificatore standard

    Un qualificatore standard è un qualificatore definito da WMI e comunemente utilizzato nel codice MOF. Ad esempio, i qualificatori [**dinamici**](dynamic-qualifier.md) e di [**lettura**](standard-qualifiers.md) sono entrambi qualificatori standard. Per ulteriori informazioni, vedere [qualificatori WMI](wmi-qualifiers.md).

-   Qualificatore CIM

    Un qualificatore CIM è un qualificatore incluso nella specifica CIM. Sebbene usino i qualificatori CIM nel codice MOF, i qualificatori standard sono progettati specificamente con WMI. Per ulteriori informazioni, vedere la [specifica DMTF CIM](https://www.dmtf.org/spec/cims.html/).

-   Qualificatore univoco

    Un qualificatore univoco è un qualificatore definito in modo specifico per una nuova classe da un provider di classi. Ad esempio, il qualificatore [**unità**](standard-qualifiers.md) è un qualificatore specifico del provider non standard. È possibile creare qualificatori personalizzati da usare con il provider. Per ulteriori informazioni sulla creazione di un provider, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).

Indipendentemente dal qualificatore, il processo principale da eseguire è usare il qualificatore nel codice MOF. Per ulteriori informazioni, vedere [applying a Qualifier](applying-a-qualifier.md). È possibile descrivere ulteriormente un qualificatore con una versione del qualificatore. Una versione qualificatore contiene ulteriori informazioni sulla modalità di utilizzo di un qualificatore da un provider. Per ulteriori informazioni, vedere [Descrizione di un qualificatore con una versione del qualificatore](describing-a-qualifier-with-a-qualifier-flavor.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



