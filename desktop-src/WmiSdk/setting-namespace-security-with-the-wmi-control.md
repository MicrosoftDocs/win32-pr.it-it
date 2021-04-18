---
description: Il controllo WMI è uno snap-in di MMC disponibile nel pannello di controllo e viene utilizzato per impostare manualmente la sicurezza dello spazio dei nomi WMI in un computer locale. È inoltre possibile impostare lo spazio dei nomi predefinito per lo scripting.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Impostazione della sicurezza dello spazio dei nomi con il controllo WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318526"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Impostazione della sicurezza dello spazio dei nomi con il controllo WMI

Il controllo WMI è uno snap-in di MMC disponibile nel **Pannello di controllo** e viene utilizzato per impostare manualmente la sicurezza dello spazio dei nomi WMI in un computer locale. È inoltre possibile impostare lo spazio dei nomi predefinito per lo scripting.


Nella procedura riportata di seguito viene descritto come individuare il controllo WMI.

**Per individuare il controllo WMI**

1.  Nel **Pannello di controllo** fare doppio clic su **strumenti di amministrazione**.
2.  Nella finestra **Strumenti di amministrazione** fare doppio clic su **Gestione computer**.
3.  Nella finestra **Gestione computer** espandere l'albero **Servizi e applicazioni** , quindi fare doppio clic sul **controllo WMI**.
4.  Fare clic con il pulsante destro del mouse sull'icona del **controllo WMI** e scegliere **Proprietà**.

Nella procedura seguente viene descritto come utilizzare il controllo WMI per configurare la sicurezza per uno spazio dei nomi come modello, quindi ottenere a livello di codice le impostazioni di sicurezza per impostare la sicurezza per altri spazi dei nomi.

**Per impostare la sicurezza dello spazio dei nomi con il controllo WMI**

1.  Creare un nuovo spazio dei nomi utilizzando il codice Managed Object Format (MOF).
2.  Eseguire il controllo WMI per impostare la sicurezza del nuovo spazio dei nomi. Dal menu **Start** fare clic su **Esegui** e digitare **wmimgmt. msc** o vedere [individuazione del controllo WMI](#).
3.  Nel riquadro di **controllo WMI** fare clic con il pulsante destro del mouse su **controllo WMI**, scegliere **Proprietà**, quindi selezionare la scheda **sicurezza** .
4.  Passare al nuovo spazio dei nomi, fare clic su **sicurezza** e quindi configurare gruppi e autorizzazioni per lo spazio dei nomi.

È inoltre possibile utilizzare Strumentazione gestione Windows Command-Line ([wmic](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) per impostare la sicurezza dello spazio dei nomi. Per ulteriori informazioni, vedere [**wmic**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Impostazione dello spazio dei nomi predefinito per gli script

Se uno script non si connette in modo esplicito a uno spazio dei nomi durante la connessione a WMI, WMI utilizza lo spazio dei nomi predefinito specificato in questo controllo. Il valore predefinito è disponibile anche nella voce del registro di sistema, come indicato di seguito:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Poiché lo spazio dei nomi predefinito è facile da modificare, con questo controllo o a livello di codice chiamando i metodi di [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specificare lo spazio dei nomi durante la connessione a WMI tramite il [moniker](constructing-a-moniker-string.md) o le chiamate a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md)

**Per impostare lo spazio dei nomi predefinito per gli script**

1.  Nella finestra **proprietà del controllo WMI** scegliere la scheda **Avanzate** .
2.  Fare clic sul pulsante **Cambia** e selezionare lo spazio dei nomi da impostare come predefinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione di descrittori di sicurezza dello spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
