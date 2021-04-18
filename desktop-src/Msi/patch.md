---
description: Il programma di installazione imposta la proprietà PATCH su un elenco di patch da applicare chiamando MsiApplyPatch, MsiApplyMultiplePatches o l'opzione della riga di comando/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: PATCH (proprietà)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331055"
---
# <a name="patch-property"></a>PATCH (proprietà)

Il programma di installazione imposta la proprietà **patch** su un elenco di patch da applicare chiamando [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) o l' [opzione della riga di comando](command-line-options.md)/p. È inoltre possibile impostare la proprietà **patch** nella riga di comando durante l'installazione di un pacchetto tramite [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) o l'opzione della riga di comando/i.

Il valore della proprietà **patch** è un elenco delle patch installate. Ogni patch nell'elenco è rappresentata dal percorso completo del pacchetto della patch (file con estensione msp). I percorsi completi nell'elenco sono separati da punti e virgola.

**Windows Installer 2,0:** Non sono supportate più patch. Per applicare più patch, è necessario Windows Installer 3,0.

## <a name="remarks"></a>Commenti

Se si crea un pacchetto di patch usando [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md) è possibile specificare che un'azione o una finestra di dialogo viene eseguita solo quando viene applicata una particolare patch. Quando si crea il pacchetto di patch, ad esempio test. msp, si crea un'immagine aggiornata del prodotto e un file delle proprietà di creazione patch. Quando si crea il file delle proprietà di creazione patch, è possibile immettere un nome di proprietà, ad esempio PATCHFORTEST, nel campo MediaSrcPropName della tabella [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) . Quando si creano le tabelle di sequenza dell'immagine aggiornata del prodotto, è possibile includere nella colonna condizione della tabella di sequenza un'istruzione condizionale per l'azione o la finestra di dialogo che si desidera rendere condizionale.

È ad esempio possibile utilizzare l'istruzione condizionale seguente per eseguire un'azione o una finestra di dialogo solo quando viene applicato test. msp.

<dl> PATCH E PATCHFORTEST E PATCH >< PATCHFORTEST  
</dl>

> [!Note]  
> Poiché la proprietà **patch** può contenere più patch, utilizzare l'operatore Substring "><" per verificare la presenza di una patch particolare anziché dell'operatore Equals "=". Per ulteriori informazioni sulle istruzioni condizionali, vedere la sezione [sintassi dell'istruzione condizionale](conditional-statement-syntax.md) .

 

Se si applica un elenco di patch che include test. msp, il programma di installazione imposta entrambe le proprietà. Ad esempio, è possibile usare l' [opzione della riga di comando](command-line-options.md) /p per applicare un elenco di due patch.

**msiexec/qb/p \\ \\ Scratch \\ Scratch \\ xyz \\ patches \\ test. msp; \\ \\ Scratch \\ Scratch \\ xyz \\ bar. msp**

Il programma di installazione imposta le proprietà **patch** e PATCHFORTEST come indicato di seguito.

<dl> PATCH = Scratch \\ \\ \\ Scratch \\ xyz \\ patches \\ test. msp; \\ \\ Scratch \\ Scratch \\ xyz \\ bar. msp  
PATCHFORTEST = \\ \\ Scratch \\ Scratch \\ xyz \\ patches \\ test. msp  
</dl>

In questo caso, la condizione è TRUE e l'azione condizionale o la finestra di dialogo precedente può essere eseguita per ogni patch installata, test. msp e bar. msp.

Se test. msp non viene applicato, il programma di installazione non lo include nella proprietà **patch** e non imposta PATCHFORTEST. In questo caso, la condizione precedente è FALSE e l'azione condizionale o la finestra di dialogo non viene eseguita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP. Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà](properties.md)
</dt> <dt>

[Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
</dt> <dt>

[Esempi di sintassi di istruzioni condizionali](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




