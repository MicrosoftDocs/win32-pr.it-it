---
description: ICE80 verifica che il valore della proprietà di riepilogo del modello ( \_ modello PID) specifichi correttamente &\# 0034; Intel64&\# 0034;, &\# 0034; x64&\# 0034; o &\# 0034; Intel&\# 0034; a seconda della presenza di componenti a 64 bit o script di azione personalizzata.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5233f260e9cc248bdb2d0c19b47956a2b7dbe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308189"
---
# <a name="ice80"></a>ICE80

ICE80 verifica che il valore della proprietà di [**Riepilogo del modello**](template-summary.md) ( \_ modello PID) specifichi correttamente "Intel64", "x64", "Arm64" o "Intel", a seconda della presenza di componenti a 64 bit o script di azione personalizzati. ICE80 controlla la [tabella](component-table.md) dei componenti con l'attributo **msidbComponentAttributes64bit** e controlla la [tabella CustomAction](customaction-table.md) per tutti gli script con l'attributo **msidbCustomActionType64BitScript** . ICE80 verifica che un pacchetto con "Intel64", "x64" o "Arm64" nella proprietà di **Riepilogo del modello** includa anche una proprietà di riepilogo del [**conteggio delle pagine**](page-count-summary.md) (PID \_ PageCount) di almeno 150.

ICE80 verifica inoltre che l'ID lingua specificato dalla proprietà [**ProductLanguage**](productlanguage.md) debba essere contenuto nella proprietà di [**Riepilogo del modello**](template-summary.md) .

Per ulteriori informazioni, vedere [Windows Installer nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md).

## <a name="result"></a>Risultato

ICE80 invia i seguenti errori.



| Errore                                                                                                                                                                   | Descrizione                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Questo pacchetto contiene il componente a 64 bit ' \[ 1 \] ', ma la proprietà di [**Riepilogo del modello**](template-summary.md) non contiene Intel64, x64 o Arm64.                    | La [tabella Component](component-table.md)contiene un componente con l'attributo **msidbComponentAttributes64bit** e la proprietà [**Summary del modello**](template-summary.md) non contiene Intel64, x64 o Arm64.        |
| Questo pacchetto contiene lo script dell'azione personalizzata a 64 bit ' \[ 1 \] ', ma la proprietà di [**Riepilogo del modello**](template-summary.md) non contiene Intel64, x64 o Arm64.         | La [tabella CustomAction](customaction-table.md) contiene un'azione personalizzata script con **msidbCustomActionType64BitScript** , ma la proprietà di [**Riepilogo del modello**](template-summary.md) non contiene Intel64, x64 o Arm64. |
| Valore non valido nel flusso di informazioni di riepilogo per% s.                                                                                                                         | Restituito per la \_ proprietà del modello PID se tale proprietà è una stringa vuota o non è un \_ tipo LPSTR VT. Restituito per \_ il PID PageCount se tale proprietà non è un \_ tipo VT i4.<br/>                                         |
| Questo pacchetto è contrassegnato con Intel64, ma ha uno schema inferiore a 150.                                                                                                  | La \_ proprietà del modello PID del pacchetto è Intel64, ma la relativa \_ proprietà di PageCount PID è inferiore a 150.                                                                                                            |
| Questo pacchetto è contrassegnato con x64 ma ha uno schema inferiore a 200.                                                                                                      | La \_ proprietà del modello PID del pacchetto è x64, ma la relativa \_ proprietà di PageCount PID è inferiore a 200.                                                                                                            |
| Questo pacchetto è contrassegnato con Arm64, ma ha uno schema inferiore a 500.                                                                                                    | La \_ proprietà del modello PID del pacchetto è Arm64, ma la relativa \_ proprietà di PageCount PID è inferiore a 500.                                                                                                            |
| Questo pacchetto a 32 bit usa la proprietà \[ 1 bit 64\]                                                                                                                       | Un pacchetto a 32 bit usa una proprietà a 64 bit.                                                                                                                                                                              |
| Questo pacchetto a 32 bit usa il tipo di localizzatore bit 64 nella voce di tabella RegLocator \[ 1\]                                                                                         | Un pacchetto a 32 bit contiene **msidbLocatorType64bit** nel campo Type della [tabella RegLocator](reglocator-table.md).                                                                                                    |
| Questo 64BitComponent \[ 1 \] USA 32BitDirectory \[ 3\]                                                                                                                     | Un componente a 64 bit usa una directory a 32 bit.                                                                                                                                                                           |
| Questo 32BitComponent \[ 1 \] USA 64BitDirectory \[ 3\]                                                                                                                     | Un componente a 32 bit usa una directory a 64 bit.                                                                                                                                                                           |
| Il valore della proprietà'[**ProductLanguage**](productlanguage.md)' nella tabella delle proprietà è' \[ 2 \] ', che non è contenuto nel flusso di proprietà di riepilogo del modello. | Il valore della proprietà [**ProductLanguage**](productlanguage.md) non è elencato nella proprietà di [**Riepilogo del modello**](template-summary.md) .                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> <dt>

[Windows Installer su sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




