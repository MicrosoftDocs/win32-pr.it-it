---
description: Consente di registrare un computer in una gerarchia di certificati utilizzando un modello, un nome visualizzato del certificato e la descrizione del certificato.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: enrollSimpleMachineCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313719"
---
# <a name="enrollsimplemachinecert"></a>enrollSimpleMachineCert

Nell'esempio enrollSimpleMachineCert viene registrato un computer in una gerarchia di certificati utilizzando un modello, un nome visualizzato del certificato e la descrizione del certificato.

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, per impostazione predefinita viene installata una versione C++ dell'esempio, nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate di registrazione del certificato \\ VC \\ EnrollSimpleMachineCert. Una versione di VBScript viene installata nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate registrazione del certificato \\ vbs \\ EnrollSimpleMachineCert.

## <a name="discussion"></a>Discussione

Esempio enrollSimpleMachineCert:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome del modello, un nome visualizzato del certificato e una descrizione del certificato.
2.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il modello specificato nella riga di comando. Il valore ContextAdministratorForceMachine per il primo parametro specifica che il certificato viene richiesto da un amministratore che agisce per conto di un computer.
3.  Aggiunge il nome visualizzato e la descrizione all'oggetto di registrazione.
4.  Tenta di registrare la richiesta di certificato e controlla lo stato del processo. La funzione checkEnrollStatus è definita in enrollCommon. cpp.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 



