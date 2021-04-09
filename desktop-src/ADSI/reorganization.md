---
title: Riorganizzazione
description: L'organizzazione vendite è stata spostata in una nuova organizzazione \ 8212; \ 0034; Vendite e supporto. \ 0034; Julie Bankert è stato promosso a vicepresidente e avrà la nuova organizzazione.
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- Riorganizzazione di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044059"
---
# <a name="reorganization"></a>Riorganizzazione

L'organizzazione vendite è stata spostata in una nuova organizzazione, ovvero "vendite e supporto". Julie Bankert è stato promosso a vicepresidente e avrà la nuova organizzazione. Joe worden, l'amministratore dell'organizzazione, deve spostare l'unità organizzativa vendite in una nuova unità organizzativa, vendite e supporto.


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



Con questo esempio di codice, tutti gli oggetti nell'unità organizzativa Sales, incluse le unità organizzative secondarie, vengono spostati nella nuova unità organizzativa.

Ora Joe può spostare Julie nell'unità organizzativa Sales and support.


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



Tenere presente che il collegamento Manager-Direct report tra Julie Bankert e Chris Gray viene aggiornato automaticamente da Active Directory.

**Per creare un report Active Directory**

1.  Aprire Visual Basic versione 6,0 e, quando viene richiesto il tipo di progetto, selezionare **progetto dati**.
2.  In **progetto dati** fare doppio clic su **dati Environment1**.
3.  Nella finestra **ambiente dati** fare clic con il pulsante destro del mouse sull'oggetto connessione **(Connection1)** e scegliere **proprietà**.
4.  Selezionare **OLE DB provider per servizi directory Microsoft**, quindi fare clic su **Avanti**.
5.  Selezionare **Usa sicurezza integrata di Windows NT**, quindi fare clic su **OK**. Viene creato un oggetto Connection.
6.  Fare di nuovo clic con il pulsante destro del mouse sulla finestra **ambiente dati** per selezionare **Aggiungi comando**. Fare clic con il pulsante destro del mouse sull'oggetto **Command1** e scegliere **Proprietà**. Verrà visualizzata la finestra di dialogo **Proprietà Command1** seguente.

    ![finestra di dialogo Proprietà Command1](images/adadsi3.png)

7.  Fare clic sul pulsante di opzione **istruzione SQL** e digitare quanto segue:

    SELECT Name, telephoneNumber FROM "LDAP://DC = Fabrikam, DC = com" WHERE objectCategory = "person" e objectClass = "User"

    Viene creato l'oggetto **Command** . Aggiungere l'oggetto **Command** al report.

8.  Fare doppio clic su **Data Report1** dalla finestra del **progetto** .
9.  Trascinare l'oggetto **Command1** dalla finestra **DataEnvironment1** nella sezione **Dettagli** della finestra **report dati** .
10. In **Proprietà DataReport1** selezionare **DataEnvironment1** dal menu a discesa per **origine dati** e selezionare **Command1** nel campo **DataMember** .
11. Nella finestra del progetto fare clic con il pulsante destro del mouse su **progetto dati**, quindi scegliere **Proprietà Dataproject**.
12. Nella finestra di dialogo **Proprietà progetto-** progetto, in **oggetto di avvio**, selezionare **DataReport1** dal menu a discesa. Fare clic su **OK** per salvare.
13. Compilazione. Verrà visualizzata la finestra di dialogo **DataReport1** seguente.

    ![finestra di dialogo DataReport1](images/adadsi4.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unione di dati eterogenei](joining-heterogeneous-data.md)
</dt> </dl>

 

 




