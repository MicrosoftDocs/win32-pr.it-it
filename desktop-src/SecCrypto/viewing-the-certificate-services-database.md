---
description: L'interfaccia ICertView viene utilizzata dai client autorizzati correttamente per visualizzare il database di Servizi certificati.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Visualizzazione del database dei servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131723"
---
# <a name="viewing-the-certificate-services-database"></a>Visualizzazione del database dei servizi certificati

L'interfaccia [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) viene utilizzata dai client autorizzati correttamente per visualizzare il database di Servizi certificati. Si noti che, come parte del prodotto spedito, è possibile utilizzare lo snap-in MMC dell'autorità di certificazione per visualizzare il database di Servizi certificati. [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) è disponibile per la visualizzazione a livello di codice del database. Il supporto per l'interfaccia **ICertView** inizia con Windows XP.

Un client autorizzato correttamente indica un utente a cui è stata concessa l'autorizzazione per visualizzare il database dei servizi certificati; lo snap-in di MMC dell'autorità di certificazione può essere utilizzato per concedere o limitare l'accesso per visualizzare il database (in **Proprietà** dell' [*autorità di certificazione*](../secgloss/c-gly.md), fare clic sulla scheda **sicurezza** ). Inoltre, per usare l'oggetto [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , è necessario che la workstation client abbia installato i componenti client di Servizi certificati.

Sebbene esistano diversi scenari per l'uso di [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) e delle interfacce correlate, di seguito viene illustrata una possibile sequenza per lo sviluppo di un'applicazione client basata su **ICertView**:

**Per visualizzare il database di Servizi certificati**

1.  Dopo aver ottenuto un'istanza dell'oggetto [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , chiamare [**ICertView:: OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) per comunicare con un' [*autorità di certificazione*](../secgloss/c-gly.md) in un computer specifico.
2.  Chiamare [**ICertView:: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) per specificare il numero di colonne nella vista; Questa chiamata viene usata anche per specificare una visualizzazione predefinita. Se nella chiamata non è specificata una visualizzazione predefinita, il chiamante deve chiamare [**ICertView:: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) per ogni colonna da contenere nella vista.
3.  facoltativo. Specificare i criteri di ordinamento e/o i criteri idonei per la query di database chiamando la funzione [**ICertView:: serestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) . I criteri validi sono costituiti dall'informata della vista per il recupero di dati in base a qualificatori quali maggiore di, minore di, uguale a e così via.
4.  Chiamare [**ICertView:: OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) per recuperare i dati nella vista; i dati della visualizzazione costituiranno le colonne richieste per mezzo di [**ICertView:: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (e se non è stata specificata una visualizzazione predefinita, [**ICertView:: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Se è stato chiamato [**ICertView:: serestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) , i dati nelle colonne verranno ordinati e/o qualificati. **ICertView:: OpenView** crea un oggetto [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) , che può essere usato per enumerare le righe della vista.
5.  Usare i [](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) metodi IEnumCERTVIEWROW [**IEnumCERTVIEWROW:: EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**IEnumCERTVIEWROW:: EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)e [**IEnumCERTVIEWROW:: EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) per recuperare i dati di attributo, colonna ed estensione nel modo desiderato.

 

 
