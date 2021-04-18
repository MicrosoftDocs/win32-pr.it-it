---
description: La proprietà ProductLanguage specifica la lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state create nel database.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Proprietà ProductLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330616"
---
# <a name="productlanguage-property"></a>Proprietà ProductLanguage

La proprietà **ProductLanguage** specifica la lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state create nel database. Questa proprietà deve essere un identificatore di lingua numerico (LANGID). Se una trasformazione modifica la lingua dell'interfaccia utente nel database, deve anche modificare il valore di questa proprietà per riflettere il nuovo linguaggio.

Questa proprietà è obbligatoria.

## <a name="remarks"></a>Commenti

Il valore della proprietà **ProductLanguage** deve essere una delle lingue elencate nella proprietà di [**Riepilogo del modello**](template-summary.md) .

Quando si crea un pacchetto come indipendente dalla lingua, impostare la proprietà **ProductLanguage** su 0 e usare il tipo di carattere MS Shell Dlg come stile di testo per tutte le finestre di dialogo Create. Poiché alcuni tipi di carattere non supportano tutti i set di caratteri, tramite questo tipo di carattere è possibile verificare che il testo venga visualizzato correttamente in tutte le versioni localizzate del sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




