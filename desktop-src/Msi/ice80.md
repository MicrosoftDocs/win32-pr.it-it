---
description: ICE80 verifica che il valore della proprietà di riepilogo del modello (TEMPLATE PID) specifichi correttamente \_ &\# 0034;Intel64&\# 0034;, &\# 0034;x64&\# 0034; o &\# 0034;Intel&\# 0034; a seconda della presenza di componenti a 64 bit o script di azioni personalizzate.
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7be298e406db40b76a54eadbe12e99175e0058d97c4d57c5a4b1cd842b000f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339941"
---
# <a name="ice80"></a>ICE80

ICE80 verifica che il valore di [**Template Summary**](template-summary.md) Property (PID TEMPLATE) specifichi correttamente \_ "Intel64", "x64", "Arm64" o "Intel" a seconda della presenza di componenti a 64 bit o script di azione personalizzati. ICE80 controlla [](component-table.md) la tabella dei componenti per tutti i componenti con l'attributo **msidbComponentAttributes64bit** e controlla la tabella [CustomAction](customaction-table.md) per eventuali script con l'attributo **msidbCustomActionType64BitScript.** ICE80 verifica che un pacchetto con "Intel64", "x64" o  "Arm64" [](page-count-summary.md) nella proprietà riepilogo modello abbia anche una proprietà di riepilogo del conteggio delle pagine (PID \_ PAGECOUNT) di almeno 150.

ICE80 convalida anche che l'ID lingua specificato dalla [**proprietà ProductLanguage**](productlanguage.md) deve essere contenuto nella [**proprietà Riepilogo**](template-summary.md) modello.

Per altre informazioni, vedere [Windows Installer in sistemi operativi a 64 bit.](windows-installer-on-64-bit-operating-systems.md)

## <a name="result"></a>Risultato

ICE80 registra gli errori seguenti.



| Errore                                                                                                                                                                   | Descrizione                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Questo pacchetto contiene il componente a 64 bit ' 1 ', ma la proprietà riepilogo modello non \[ \] contiene Intel64, x64 o Arm64. [](template-summary.md)                    | La [tabella dei](component-table.md)componenti contiene un componente con l'attributo **msidbComponentAttributes64bit** e la proprietà [**riepilogo**](template-summary.md) modello non contiene Intel64, x64 o Arm64.        |
| Questo pacchetto contiene lo script di azione personalizzata a 64 bit ' 1 ', ma la proprietà di riepilogo del modello non \[ \] contiene Intel64, x64 o Arm64. [](template-summary.md)         | [La tabella CustomAction](customaction-table.md) contiene un'azione personalizzata script con **msidbCustomActionType64BitScript,** ma la proprietà [**riepilogo**](template-summary.md) modello non contiene Intel64, x64 o Arm64. |
| Valore non valido nel flusso di informazioni di riepilogo per %s.                                                                                                                         | Restituito per la proprietà TEMPLATE PID se tale proprietà è una stringa vuota o \_ non è di tipo \_ VT LPSTR. Restituito per PID \_ PAGECOUNT se la proprietà non è di tipo VT \_ I4.<br/>                                         |
| Questo pacchetto è contrassegnato con Intel64 ma ha uno schema minore di 150.                                                                                                  | La proprietà \_ TEMPLATE PID del pacchetto è Intel64, ma la relativa proprietà PID \_ PAGECOUNT è minore di 150.                                                                                                            |
| Questo pacchetto è contrassegnato con x64 ma ha uno schema minore di 200.                                                                                                      | La proprietà TEMPLATE \_ PID del pacchetto è x64, ma la relativa proprietà PID \_ PAGECOUNT è minore di 200.                                                                                                            |
| Questo pacchetto è contrassegnato con Arm64 ma ha uno schema minore di 500.                                                                                                    | La proprietà TEMPLATE \_ PID del pacchetto è Arm64, ma la relativa proprietà PID \_ PAGECOUNT è minore di 500.                                                                                                            |
| Questo pacchetto a 32 bit usa la proprietà a 64 bit \[ 1\]                                                                                                                       | Un pacchetto a 32 bit usa una proprietà a 64 bit.                                                                                                                                                                              |
| Questo pacchetto a 32 bit usa il tipo di localizzatore a 64 bit nella voce 1 della tabella RegLocator \[\]                                                                                         | Un pacchetto a 32 bit contiene **msidbLocatorType64bit** nel campo Tipo della [tabella RegLocator](reglocator-table.md).                                                                                                    |
| Questo 64BitComponent \[ 1 \] usa 32BitDirectory \[ 3\]                                                                                                                     | Un componente a 64 bit usa una directory a 32 bit.                                                                                                                                                                           |
| Questo 32BitComponent \[ 1 \] usa 64BitDirectory \[ 3\]                                                                                                                     | Un componente a 32 bit usa una directory a 64 bit.                                                                                                                                                                           |
| La proprietà '[**ProductLanguage**](productlanguage.md)' nella tabella Property ha un valore ' 2 ', che non \[ è contenuto nel flusso della proprietà riepilogo \] modello. | Il valore della proprietà [**ProductLanguage**](productlanguage.md) non è elencato nella [**proprietà Riepilogo**](template-summary.md) modello.                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> <dt>

[Windows Programma di installazione nei sistemi operativi a 64 bit](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




