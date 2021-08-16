---
description: Come molte altre tecniche in Managed Object Format (MOF), l'applicazione di un qualificatore al codice è un processo relativamente semplice.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Applicazione di un qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a393c7d3764338a8365ad3959803a8a3f665dbf1b9bdb0bebaaa7121ee6cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320138"
---
# <a name="applying-a-qualifier"></a>Applicazione di un qualificatore

Come molte altre tecniche in Managed Object Format (MOF), l'applicazione di un qualificatore al codice è un processo relativamente semplice.

Le uniche sfide reali sono le restrizioni seguenti nelle convenzioni di denominazione applicate da WMI:

-   Un qualificatore può descrivere una classe, un'istanza, una proprietà, un metodo o un parametro di metodo.
-   I nomi dei qualificatori non possono contenere caratteri di sottolineatura iniziali o finali.
-   Un nome di qualificatore non può iniziare con una cifra.
-   Un nome di qualificatore non può contenere caratteri speciali, ad esempio & \* @ ! ~ \\ /.
-   Per tutti i nomi di qualificatore non viene fatto distinzione tra maiuscole e minuscole.
-   Non è possibile ridefinire i qualificatori WMI standard o i qualificatori descritti nella specifica CIM DMTF.
-   I tipi di qualificatore non vengono dichiarati in modo esplicito.

    Se non si dichiara un tipo qualificatore, WMI presuppone che il tipo sia booleano con valore **TRUE**. In caso contrario, i qualificatori dei tipi WMI si basano sui valori del qualificatore dichiarati.

-   Quando si creano qualificatori personalizzati, è necessario antesare il nome dello schema al nome del qualificatore.

    Lo scopo di questa regola è evitare confusione con i nuovi qualificatori.

-   È possibile creare matrici omogenee di qualificatori.

    Nell'esempio di codice seguente viene illustrato come le matrici di qualificatori vengono specificate con parentesi graffe che circondano i valori.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI non supporta i tipi di automazione non elencati nel riferimento, ad esempio VT \_ NULL. Per altre informazioni, vedere [Tipi di dati MOF](mof-data-types.md).

La procedura seguente consente di usare C++ per aggiungere un qualificatore a una proprietà.

**Per applicare un qualificatore usando C++**

-   Applicare il qualificatore con una chiamata al [**metodo IWbemQualifierSet::P ut.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put)

    È possibile usare altri metodi di [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) per recuperare o eliminare qualificatori esistenti.

La procedura seguente consente di applicare un qualificatore nei file MOF.

**Per descrivere una parola chiave o un identificatore con un qualificatore tramite MOF**

-   Inserire un qualificatore tra parentesi prima della parola chiave o dell'identificatore descritto dal qualificatore.

    Nell'esempio di codice seguente viene illustrato come vengono usati i qualificatori.

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    Nell'esempio seguente viene descritta la corretta posizione dei qualificatori.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



