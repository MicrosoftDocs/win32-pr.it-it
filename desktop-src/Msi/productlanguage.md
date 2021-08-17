---
description: La proprietà ProductLanguage specifica la lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state scritte nel database.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: ProductLanguage - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd2a079767b1e39f07bdcf90f2a359604d89ccf9e394d2695b5aa74cc9e459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376456"
---
# <a name="productlanguage-property"></a>ProductLanguage - proprietà

La **proprietà ProductLanguage** specifica la lingua che il programma di installazione deve usare per le stringhe nell'interfaccia utente che non sono state scritte nel database. Questa proprietà deve essere un identificatore di lingua numerico (LANGID). Se una trasformazione modifica la lingua dell'interfaccia utente nel database, è necessario modificare anche il valore di questa proprietà per riflettere la nuova lingua.

Questa proprietà è REQUIRED.

## <a name="remarks"></a>Commenti

Il valore della **proprietà ProductLanguage** deve essere una delle lingue elencate nella [**proprietà Riepilogo**](template-summary.md) modello.

Quando si crea un pacchetto come indipendente dalla lingua, impostare la proprietà **ProductLanguage** su 0 e usare il tipo di carattere MS Shell Dlg come stile di testo per tutte le finestre di dialogo scritte. Poiché alcuni tipi di carattere non supportano tutti i set di caratteri, usando questo tipo di carattere è possibile assicurarsi che il testo venga visualizzato correttamente in tutte le versioni localizzate del sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP. Vedere i [Windows di installazione Run-Time](windows-installer-portal.md) per informazioni sul Service Pack Windows minimo richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> </dl>

 

 




