---
title: Riorganizzazione
description: L'organizzazione di vendita è passata a una nuova organizzazione \ 8212; \ 0034; Vendite e supporto. \ 0034; Julie Bankert è stata promossa a vicepresidenza e sarà alla guida della nuova organizzazione.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Riorganizzazione di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368b4db1909c50242e3eda1402e46896e54785aa66739b324995b7edbdd1b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690758"
---
# <a name="reorganization"></a>Riorganizzazione

L'organizzazione di vendita è passata a una nuova organizzazione, ovvero "Vendite e supporto". Julie Bankert è stata promossa a vicepresidenza e sarà alla guida della nuova organizzazione. Joe Worden, amministratore dell'organizzazione, deve spostare l'unità organizzativa Sales in una nuova unità organizzativa, Sales and Support.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Con questo esempio di codice, tutti gli oggetti nell'unità organizzativa sales, incluse le unità organizzative secondarie, vengono spostati nella nuova unità organizzativa.

A questo punto, Joe può spostare Julie nell'unità organizzativa Vendite e supporto.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Tenere presente che il collegamento diretto al report tra Julie Bankert e Chris Gray viene aggiornato automaticamente da Active Directory.

**Per creare un report di Active Directory**

1.  Aprire Visual Basic versione 6.0 e, quando viene richiesto il tipo di **progetto,** selezionare Data Project .
2.  In **Data Project** fare doppio clic su Data **Environment1**.
3.  Nella finestra **Ambiente dati fare** clic con il pulsante destro del mouse sull'oggetto connessione **(Connection1)** e scegliere **Proprietà**.
4.  Selezionare **OLE DB provider di servizi directory Microsoft** e fare clic su **Avanti.**
5.  Selezionare **Usa Windows NT sicurezza integrata** e fare clic su **OK.** Verrà creato un oggetto connessione.
6.  Fare di nuovo clic con il **pulsante destro del mouse** sulla finestra Data Environment per selezionare Aggiungi **comando**. Fare clic con il pulsante destro **del mouse sull'oggetto Command1** e **scegliere Proprietà**. Verrà visualizzata la finestra di dialogo Proprietà **command1** seguente.

    ![Finestra di dialogo delle proprietà command1](images/adadsi3.png)

7.  Fare clic **SQL pulsante di opzione** Istruzione di configurazione e digitare quanto segue:

    SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'

    Viene **creato** l'oggetto Command. Aggiungere **l'oggetto** Command al report.

8.  Fare doppio clic **su Data Report1** **nella finestra Project** dati.
9.  Trascinare **l'oggetto Command1** **dalla finestra DataEnvironment1** alla sezione **Dettagli** della finestra **Report di** dati.
10. In **Proprietà DataReport1** per **DataSource** selezionare **DataEnvironment1** dal menu a discesa e selezionare **Command1** nel **campo DataMember.**
11. Nella finestra del progetto fare clic con il pulsante destro **del mouse** su Project dati e scegliere **Proprietà dataprogetto**.
12. Nella finestra **di dialogo DataProject - Project proprietà** , in Oggetto **di** avvio selezionare **DataReport1** dal menu a discesa. Fare clic su **OK** per salvare.
13. Compilazione. Verrà visualizzata **la finestra di dialogo DataReport1** seguente.

    ![Finestra di dialogo datareport1](images/adadsi4.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unione di dati eterogenei](joining-heterogeneous-data.md)
</dt> </dl>

 

 




