---
description: Analogamente a molte altre tecniche in Managed Object Format (MOF), l'applicazione di un qualificatore al codice è un processo relativamente semplice.
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: Applicazione di un qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760778"
---
# <a name="applying-a-qualifier"></a>Applicazione di un qualificatore

Analogamente a molte altre tecniche in Managed Object Format (MOF), l'applicazione di un qualificatore al codice è un processo relativamente semplice.

Le convenzioni di denominazione applicate da WMI sono le seguenti:

-   Un qualificatore può descrivere una classe, un'istanza, una proprietà, un metodo o un parametro del metodo.
-   I nomi dei qualificatori non possono contenere caratteri di sottolineatura iniziali o finali.
-   Un nome di qualificatore non può iniziare con una cifra.
-   Un nome qualificatore non può contenere caratteri speciali, ad esempio & \* @! ~ \\ /.
-   Tutti i nomi dei qualificatori non fanno distinzione tra maiuscole e minuscole.
-   Non è possibile ridefinire i qualificatori WMI standard o i qualificatori descritti nella specifica DMTF CIM.
-   I tipi qualificatore non sono dichiarati in modo esplicito.

    Se non si dichiara un tipo di qualificatore, WMI presuppone che il tipo sia booleano con un valore **true**. In caso contrario, i qualificatori dei tipi WMI sono basati sui valori del qualificatore dichiarati.

-   Quando si creano i propri qualificatori, è necessario anteporre al nome del qualificatore il nome dello schema.

    Lo scopo di questa regola è evitare confusione con i nuovi qualificatori.

-   È possibile creare matrici omogenee di qualificatori.

    Nell'esempio di codice riportato di seguito viene illustrato come specificare matrici di qualificatori con parentesi graffe che racchiudono i valori.

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   WMI non supporta i tipi di automazione non elencati nel riferimento, ad esempio VT \_ null. Per ulteriori informazioni, vedere [tipi di dati MOF](mof-data-types.md).

La procedura seguente consente di usare C++ per aggiungere un qualificatore a una proprietà.

**Per applicare un qualificatore mediante C++**

-   Applicare il qualificatore con una chiamata al metodo [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    È possibile utilizzare altri metodi di [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) per recuperare o eliminare i qualificatori esistenti.

La procedura seguente consente di applicare un qualificatore nei file MOF.

**Per descrivere una parola chiave o un identificatore con un qualificatore usando MOF**

-   Posizionare un qualificatore tra parentesi quadre prima della parola chiave o dell'identificatore descritto dal qualificatore.

    Nell'esempio di codice seguente viene illustrato come vengono utilizzati i qualificatori.

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

    Nell'esempio seguente viene descritto il posizionamento appropriato dei qualificatori.

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



